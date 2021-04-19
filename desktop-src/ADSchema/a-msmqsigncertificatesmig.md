---
title: MSMQ-Sign-Zertifikats-MiG-Attribut
description: Im gemischten Modus von MSMQ enthält das-Attribut den vorherigen Wert von msmqsignzertifikats. MSMQ unterstützt die Migration von MSMQ 1,0 DS zu Windows 2000 DS, und der gemischte Modus gibt einen Status an, in dem einige der DS-Schweregrade nicht auf Windows 2000 aktualisiert wurden.
ms.assetid: 0dbc5d97-39e6-4863-a386-541ea2abaadc
ms.tgt_platform: multiple
keywords:
- MSMQ-Sign-Zertifikats-MiG-Attribut AD-Schema
- AD-Schema des msmqsigncertifitoresmig-Attributs
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates-Mig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1916cf98d15da1bd84603a2305543e899d868
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344144"
---
# <a name="msmq-sign-certificates-mig-attribute"></a><span data-ttu-id="ab303-106">MSMQ-Sign-Zertifikats-MiG-Attribut</span><span class="sxs-lookup"><span data-stu-id="ab303-106">MSMQ-Sign-Certificates-Mig attribute</span></span>

<span data-ttu-id="ab303-107">Im gemischten Modus von MSMQ enthält das-Attribut den vorherigen Wert von msmqsignzertifikats.</span><span class="sxs-lookup"><span data-stu-id="ab303-107">In MSMQ mixed-mode, the attribute contains the previous value of mSMQSignCertificates.</span></span> <span data-ttu-id="ab303-108">MSMQ unterstützt die Migration von MSMQ 1,0 DS zu Windows 2000 DS, und der gemischte Modus gibt einen Status an, in dem einige der DS-Schweregrade nicht auf Windows 2000 aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="ab303-108">MSMQ supports migration from the MSMQ 1.0 DS to the Windows 2000 DS, and mixed mode specifies a state in which some of the DS severs were not upgraded to Windows 2000.</span></span>



| <span data-ttu-id="ab303-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ab303-109">Entry</span></span> | <span data-ttu-id="ab303-110">Wert</span><span class="sxs-lookup"><span data-stu-id="ab303-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="ab303-111">CN</span><span class="sxs-lookup"><span data-stu-id="ab303-111">CN</span></span>                | <span data-ttu-id="ab303-112">MSMQ-Sign-Zertifikats-MiG</span><span class="sxs-lookup"><span data-stu-id="ab303-112">MSMQ-Sign-Certificates-Mig</span></span>                            |
| <span data-ttu-id="ab303-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ab303-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ab303-114">msmqsigncertifikatesmig</span><span class="sxs-lookup"><span data-stu-id="ab303-114">mSMQSignCertificatesMig</span></span>                               |
| <span data-ttu-id="ab303-115">Size</span><span class="sxs-lookup"><span data-stu-id="ab303-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="ab303-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ab303-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="ab303-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="ab303-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="ab303-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ab303-118">Attribute-Id</span></span>      | <span data-ttu-id="ab303-119">1.2.840.113556.1.4.967</span><span class="sxs-lookup"><span data-stu-id="ab303-119">1.2.840.113556.1.4.967</span></span>                                |
| <span data-ttu-id="ab303-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ab303-120">System-Id-Guid</span></span>    | <span data-ttu-id="ab303-121">3881b8ea-da3b-11d1-90a5-00c04f d91ab1</span><span class="sxs-lookup"><span data-stu-id="ab303-121">3881b8ea-da3b-11d1-90a5-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="ab303-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab303-122">Syntax</span></span>            | [<span data-ttu-id="ab303-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="ab303-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="ab303-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ab303-124">Implementations</span></span>

-   [<span data-ttu-id="ab303-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ab303-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ab303-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ab303-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ab303-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ab303-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ab303-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ab303-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ab303-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ab303-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ab303-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ab303-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ab303-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ab303-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ab303-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ab303-132">Entry</span></span> | <span data-ttu-id="ab303-133">Wert</span><span class="sxs-lookup"><span data-stu-id="ab303-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab303-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ab303-134">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ab303-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab303-135">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ab303-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab303-136">System-Only</span></span>            | <span data-ttu-id="ab303-137">False</span><span class="sxs-lookup"><span data-stu-id="ab303-137">False</span></span>                                                                                         |
| <span data-ttu-id="ab303-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ab303-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ab303-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab303-139">True</span></span>                                                                                          |
| <span data-ttu-id="ab303-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ab303-140">Is Indexed</span></span>             | <span data-ttu-id="ab303-141">False</span><span class="sxs-lookup"><span data-stu-id="ab303-141">False</span></span>                                                                                         |
| <span data-ttu-id="ab303-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ab303-142">In Global Catalog</span></span>      | <span data-ttu-id="ab303-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab303-143">True</span></span>                                                                                          |
| <span data-ttu-id="ab303-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ab303-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab303-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ab303-145">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ab303-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab303-146">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ab303-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab303-147">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ab303-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab303-148">Search-Flags</span></span>           | <span data-ttu-id="ab303-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab303-149">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ab303-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab303-150">System-Flags</span></span>           | <span data-ttu-id="ab303-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab303-151">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ab303-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ab303-152">Classes used in</span></span>        | [<span data-ttu-id="ab303-153">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ab303-153">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ab303-154">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ab303-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ab303-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ab303-155">Windows Server 2003</span></span>



| <span data-ttu-id="ab303-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ab303-156">Entry</span></span> | <span data-ttu-id="ab303-157">Wert</span><span class="sxs-lookup"><span data-stu-id="ab303-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab303-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ab303-158">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ab303-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab303-159">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ab303-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab303-160">System-Only</span></span>            | <span data-ttu-id="ab303-161">False</span><span class="sxs-lookup"><span data-stu-id="ab303-161">False</span></span>                                                                                         |
| <span data-ttu-id="ab303-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ab303-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ab303-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab303-163">True</span></span>                                                                                          |
| <span data-ttu-id="ab303-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ab303-164">Is Indexed</span></span>             | <span data-ttu-id="ab303-165">False</span><span class="sxs-lookup"><span data-stu-id="ab303-165">False</span></span>                                                                                         |
| <span data-ttu-id="ab303-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ab303-166">In Global Catalog</span></span>      | <span data-ttu-id="ab303-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab303-167">True</span></span>                                                                                          |
| <span data-ttu-id="ab303-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ab303-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab303-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ab303-169">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ab303-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab303-170">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ab303-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab303-171">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ab303-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab303-172">Search-Flags</span></span>           | <span data-ttu-id="ab303-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab303-173">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ab303-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab303-174">System-Flags</span></span>           | <span data-ttu-id="ab303-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab303-175">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ab303-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ab303-176">Classes used in</span></span>        | [<span data-ttu-id="ab303-177">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ab303-177">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ab303-178">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ab303-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ab303-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ab303-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ab303-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ab303-180">Entry</span></span> | <span data-ttu-id="ab303-181">Wert</span><span class="sxs-lookup"><span data-stu-id="ab303-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab303-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ab303-182">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ab303-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab303-183">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ab303-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab303-184">System-Only</span></span>            | <span data-ttu-id="ab303-185">False</span><span class="sxs-lookup"><span data-stu-id="ab303-185">False</span></span>                                                                                         |
| <span data-ttu-id="ab303-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ab303-186">Is-Single-Valued</span></span>       | <span data-ttu-id="ab303-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab303-187">True</span></span>                                                                                          |
| <span data-ttu-id="ab303-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ab303-188">Is Indexed</span></span>             | <span data-ttu-id="ab303-189">False</span><span class="sxs-lookup"><span data-stu-id="ab303-189">False</span></span>                                                                                         |
| <span data-ttu-id="ab303-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ab303-190">In Global Catalog</span></span>      | <span data-ttu-id="ab303-191">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab303-191">True</span></span>                                                                                          |
| <span data-ttu-id="ab303-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ab303-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab303-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ab303-193">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ab303-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab303-194">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ab303-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab303-195">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ab303-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab303-196">Search-Flags</span></span>           | <span data-ttu-id="ab303-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab303-197">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ab303-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab303-198">System-Flags</span></span>           | <span data-ttu-id="ab303-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab303-199">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ab303-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ab303-200">Classes used in</span></span>        | [<span data-ttu-id="ab303-201">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ab303-201">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ab303-202">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ab303-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ab303-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab303-203">Windows Server 2008</span></span>



| <span data-ttu-id="ab303-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ab303-204">Entry</span></span> | <span data-ttu-id="ab303-205">Wert</span><span class="sxs-lookup"><span data-stu-id="ab303-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab303-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ab303-206">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ab303-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab303-207">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ab303-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab303-208">System-Only</span></span>            | <span data-ttu-id="ab303-209">False</span><span class="sxs-lookup"><span data-stu-id="ab303-209">False</span></span>                                                                                         |
| <span data-ttu-id="ab303-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ab303-210">Is-Single-Valued</span></span>       | <span data-ttu-id="ab303-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab303-211">True</span></span>                                                                                          |
| <span data-ttu-id="ab303-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ab303-212">Is Indexed</span></span>             | <span data-ttu-id="ab303-213">False</span><span class="sxs-lookup"><span data-stu-id="ab303-213">False</span></span>                                                                                         |
| <span data-ttu-id="ab303-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ab303-214">In Global Catalog</span></span>      | <span data-ttu-id="ab303-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab303-215">True</span></span>                                                                                          |
| <span data-ttu-id="ab303-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ab303-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab303-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ab303-217">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ab303-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab303-218">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ab303-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab303-219">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ab303-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab303-220">Search-Flags</span></span>           | <span data-ttu-id="ab303-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab303-221">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ab303-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab303-222">System-Flags</span></span>           | <span data-ttu-id="ab303-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab303-223">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ab303-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ab303-224">Classes used in</span></span>        | [<span data-ttu-id="ab303-225">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ab303-225">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ab303-226">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ab303-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ab303-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ab303-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ab303-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ab303-228">Entry</span></span> | <span data-ttu-id="ab303-229">Wert</span><span class="sxs-lookup"><span data-stu-id="ab303-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab303-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ab303-230">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ab303-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab303-231">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ab303-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab303-232">System-Only</span></span>            | <span data-ttu-id="ab303-233">False</span><span class="sxs-lookup"><span data-stu-id="ab303-233">False</span></span>                                                                                         |
| <span data-ttu-id="ab303-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ab303-234">Is-Single-Valued</span></span>       | <span data-ttu-id="ab303-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab303-235">True</span></span>                                                                                          |
| <span data-ttu-id="ab303-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ab303-236">Is Indexed</span></span>             | <span data-ttu-id="ab303-237">False</span><span class="sxs-lookup"><span data-stu-id="ab303-237">False</span></span>                                                                                         |
| <span data-ttu-id="ab303-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ab303-238">In Global Catalog</span></span>      | <span data-ttu-id="ab303-239">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab303-239">True</span></span>                                                                                          |
| <span data-ttu-id="ab303-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ab303-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab303-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ab303-241">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ab303-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab303-242">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ab303-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab303-243">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ab303-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab303-244">Search-Flags</span></span>           | <span data-ttu-id="ab303-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab303-245">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ab303-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab303-246">System-Flags</span></span>           | <span data-ttu-id="ab303-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab303-247">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ab303-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ab303-248">Classes used in</span></span>        | [<span data-ttu-id="ab303-249">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ab303-249">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ab303-250">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ab303-250">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ab303-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ab303-251">Windows Server 2012</span></span>



| <span data-ttu-id="ab303-252">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ab303-252">Entry</span></span> | <span data-ttu-id="ab303-253">Wert</span><span class="sxs-lookup"><span data-stu-id="ab303-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab303-254">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ab303-254">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ab303-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab303-255">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="ab303-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab303-256">System-Only</span></span>            | <span data-ttu-id="ab303-257">False</span><span class="sxs-lookup"><span data-stu-id="ab303-257">False</span></span>                                                                                         |
| <span data-ttu-id="ab303-258">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ab303-258">Is-Single-Valued</span></span>       | <span data-ttu-id="ab303-259">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab303-259">True</span></span>                                                                                          |
| <span data-ttu-id="ab303-260">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ab303-260">Is Indexed</span></span>             | <span data-ttu-id="ab303-261">False</span><span class="sxs-lookup"><span data-stu-id="ab303-261">False</span></span>                                                                                         |
| <span data-ttu-id="ab303-262">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ab303-262">In Global Catalog</span></span>      | <span data-ttu-id="ab303-263">Richtig</span><span class="sxs-lookup"><span data-stu-id="ab303-263">True</span></span>                                                                                          |
| <span data-ttu-id="ab303-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ab303-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab303-265">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ab303-265">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="ab303-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab303-266">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="ab303-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab303-267">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="ab303-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab303-268">Search-Flags</span></span>           | <span data-ttu-id="ab303-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab303-269">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="ab303-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab303-270">System-Flags</span></span>           | <span data-ttu-id="ab303-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab303-271">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="ab303-272">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ab303-272">Classes used in</span></span>        | [<span data-ttu-id="ab303-273">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ab303-273">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="ab303-274">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ab303-274">**User**</span></span>](c-user.md)<br/> |



 

 





