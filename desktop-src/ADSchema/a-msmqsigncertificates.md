---
title: MSMQ-Sign-Zertifikats-Attribut
description: Dieses Attribut enthält eine Reihe von Zertifikaten. Ein Benutzer kann ein Zertifikat pro Computer generieren. Für jedes Zertifikat wird auch ein Digest beibehalten.
ms.assetid: 70e182c7-3544-43d7-b27a-6e8d03bd2d47
ms.tgt_platform: multiple
keywords:
- AD-Schema für das Attribut "MSMQ-Sign-Zertifikats"
- AD-Schema des msmqsignzertifikats-Attributs
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd7e81cf145ac249b78e0a3e20be657df68b4af
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859648"
---
# <a name="msmq-sign-certificates-attribute"></a><span data-ttu-id="2183f-107">MSMQ-Sign-Zertifikats-Attribut</span><span class="sxs-lookup"><span data-stu-id="2183f-107">MSMQ-Sign-Certificates attribute</span></span>

<span data-ttu-id="2183f-108">Dieses Attribut enthält eine Reihe von Zertifikaten.</span><span class="sxs-lookup"><span data-stu-id="2183f-108">This attribute contains a number of certificates.</span></span> <span data-ttu-id="2183f-109">Ein Benutzer kann ein Zertifikat pro Computer generieren.</span><span class="sxs-lookup"><span data-stu-id="2183f-109">A user can generate a certificate per computer.</span></span> <span data-ttu-id="2183f-110">Für jedes Zertifikat wird auch ein Digest beibehalten.</span><span class="sxs-lookup"><span data-stu-id="2183f-110">For each certificate we also keep a digest.</span></span>



| <span data-ttu-id="2183f-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2183f-111">Entry</span></span> | <span data-ttu-id="2183f-112">Wert</span><span class="sxs-lookup"><span data-stu-id="2183f-112">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2183f-113">CN</span><span class="sxs-lookup"><span data-stu-id="2183f-113">CN</span></span>                | <span data-ttu-id="2183f-114">MSMQ-Sign-Zertifikate</span><span class="sxs-lookup"><span data-stu-id="2183f-114">MSMQ-Sign-Certificates</span></span>                                                                 |
| <span data-ttu-id="2183f-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2183f-115">Ldap-Display-Name</span></span> | <span data-ttu-id="2183f-116">msmqsignzertifikate</span><span class="sxs-lookup"><span data-stu-id="2183f-116">mSMQSignCertificates</span></span>                                                                   |
| <span data-ttu-id="2183f-117">Size</span><span class="sxs-lookup"><span data-stu-id="2183f-117">Size</span></span>              | <span data-ttu-id="2183f-118">Der Attributtyp ist ein BLOB, die Größe ist nicht begrenzt, und die Daten werden in unserem eigenen Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2183f-118">The attribute type is a BLOB, size is not limited, and data is kept in our own format.</span></span> |
| <span data-ttu-id="2183f-119">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2183f-119">Update Privilege</span></span>  | \-                                                                                     |
| <span data-ttu-id="2183f-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="2183f-120">Update Frequency</span></span>  | \-                                                                                     |
| <span data-ttu-id="2183f-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2183f-121">Attribute-Id</span></span>      | <span data-ttu-id="2183f-122">1.2.840.113556.1.4.947</span><span class="sxs-lookup"><span data-stu-id="2183f-122">1.2.840.113556.1.4.947</span></span>                                                                 |
| <span data-ttu-id="2183f-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2183f-123">System-Id-Guid</span></span>    | <span data-ttu-id="2183f-124">9a0dc33b-C100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="2183f-124">9a0dc33b-c100-11d1-bbc5-0080c76670c0</span></span>                                                   |
| <span data-ttu-id="2183f-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="2183f-125">Syntax</span></span>            | [<span data-ttu-id="2183f-126">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="2183f-126">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                  |



## <a name="implementations"></a><span data-ttu-id="2183f-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="2183f-127">Implementations</span></span>

-   [<span data-ttu-id="2183f-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2183f-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2183f-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2183f-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2183f-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2183f-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2183f-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2183f-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2183f-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2183f-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2183f-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2183f-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2183f-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2183f-134">Windows 2000 Server</span></span>



| <span data-ttu-id="2183f-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2183f-135">Entry</span></span> | <span data-ttu-id="2183f-136">Wert</span><span class="sxs-lookup"><span data-stu-id="2183f-136">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2183f-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2183f-137">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2183f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2183f-138">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2183f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="2183f-139">System-Only</span></span>            | <span data-ttu-id="2183f-140">False</span><span class="sxs-lookup"><span data-stu-id="2183f-140">False</span></span>                                                                                         |
| <span data-ttu-id="2183f-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2183f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="2183f-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="2183f-142">True</span></span>                                                                                          |
| <span data-ttu-id="2183f-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2183f-143">Is Indexed</span></span>             | <span data-ttu-id="2183f-144">False</span><span class="sxs-lookup"><span data-stu-id="2183f-144">False</span></span>                                                                                         |
| <span data-ttu-id="2183f-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2183f-145">In Global Catalog</span></span>      | <span data-ttu-id="2183f-146">Richtig</span><span class="sxs-lookup"><span data-stu-id="2183f-146">True</span></span>                                                                                          |
| <span data-ttu-id="2183f-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2183f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="2183f-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2183f-148">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="2183f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2183f-149">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="2183f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2183f-150">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="2183f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2183f-151">Search-Flags</span></span>           | <span data-ttu-id="2183f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2183f-152">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="2183f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2183f-153">System-Flags</span></span>           | <span data-ttu-id="2183f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2183f-154">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="2183f-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2183f-155">Classes used in</span></span>        | [<span data-ttu-id="2183f-156">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2183f-156">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="2183f-157">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2183f-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2183f-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2183f-158">Windows Server 2003</span></span>



| <span data-ttu-id="2183f-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2183f-159">Entry</span></span> | <span data-ttu-id="2183f-160">Wert</span><span class="sxs-lookup"><span data-stu-id="2183f-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2183f-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2183f-161">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2183f-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2183f-162">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2183f-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="2183f-163">System-Only</span></span>            | <span data-ttu-id="2183f-164">False</span><span class="sxs-lookup"><span data-stu-id="2183f-164">False</span></span>                                                                                         |
| <span data-ttu-id="2183f-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2183f-165">Is-Single-Valued</span></span>       | <span data-ttu-id="2183f-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="2183f-166">True</span></span>                                                                                          |
| <span data-ttu-id="2183f-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2183f-167">Is Indexed</span></span>             | <span data-ttu-id="2183f-168">False</span><span class="sxs-lookup"><span data-stu-id="2183f-168">False</span></span>                                                                                         |
| <span data-ttu-id="2183f-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2183f-169">In Global Catalog</span></span>      | <span data-ttu-id="2183f-170">Richtig</span><span class="sxs-lookup"><span data-stu-id="2183f-170">True</span></span>                                                                                          |
| <span data-ttu-id="2183f-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2183f-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="2183f-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2183f-172">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="2183f-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2183f-173">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="2183f-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2183f-174">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="2183f-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2183f-175">Search-Flags</span></span>           | <span data-ttu-id="2183f-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2183f-176">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="2183f-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2183f-177">System-Flags</span></span>           | <span data-ttu-id="2183f-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2183f-178">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="2183f-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2183f-179">Classes used in</span></span>        | [<span data-ttu-id="2183f-180">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2183f-180">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="2183f-181">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2183f-181">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2183f-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2183f-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2183f-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2183f-183">Entry</span></span> | <span data-ttu-id="2183f-184">Wert</span><span class="sxs-lookup"><span data-stu-id="2183f-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2183f-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2183f-185">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2183f-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2183f-186">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2183f-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="2183f-187">System-Only</span></span>            | <span data-ttu-id="2183f-188">False</span><span class="sxs-lookup"><span data-stu-id="2183f-188">False</span></span>                                                                                         |
| <span data-ttu-id="2183f-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2183f-189">Is-Single-Valued</span></span>       | <span data-ttu-id="2183f-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="2183f-190">True</span></span>                                                                                          |
| <span data-ttu-id="2183f-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2183f-191">Is Indexed</span></span>             | <span data-ttu-id="2183f-192">False</span><span class="sxs-lookup"><span data-stu-id="2183f-192">False</span></span>                                                                                         |
| <span data-ttu-id="2183f-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2183f-193">In Global Catalog</span></span>      | <span data-ttu-id="2183f-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="2183f-194">True</span></span>                                                                                          |
| <span data-ttu-id="2183f-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2183f-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="2183f-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2183f-196">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="2183f-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2183f-197">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="2183f-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2183f-198">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="2183f-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2183f-199">Search-Flags</span></span>           | <span data-ttu-id="2183f-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2183f-200">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="2183f-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2183f-201">System-Flags</span></span>           | <span data-ttu-id="2183f-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2183f-202">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="2183f-203">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2183f-203">Classes used in</span></span>        | [<span data-ttu-id="2183f-204">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2183f-204">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="2183f-205">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2183f-205">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2183f-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2183f-206">Windows Server 2008</span></span>



| <span data-ttu-id="2183f-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2183f-207">Entry</span></span> | <span data-ttu-id="2183f-208">Wert</span><span class="sxs-lookup"><span data-stu-id="2183f-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2183f-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2183f-209">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2183f-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2183f-210">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2183f-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="2183f-211">System-Only</span></span>            | <span data-ttu-id="2183f-212">False</span><span class="sxs-lookup"><span data-stu-id="2183f-212">False</span></span>                                                                                         |
| <span data-ttu-id="2183f-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2183f-213">Is-Single-Valued</span></span>       | <span data-ttu-id="2183f-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="2183f-214">True</span></span>                                                                                          |
| <span data-ttu-id="2183f-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2183f-215">Is Indexed</span></span>             | <span data-ttu-id="2183f-216">False</span><span class="sxs-lookup"><span data-stu-id="2183f-216">False</span></span>                                                                                         |
| <span data-ttu-id="2183f-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2183f-217">In Global Catalog</span></span>      | <span data-ttu-id="2183f-218">Richtig</span><span class="sxs-lookup"><span data-stu-id="2183f-218">True</span></span>                                                                                          |
| <span data-ttu-id="2183f-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2183f-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="2183f-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2183f-220">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="2183f-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2183f-221">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="2183f-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2183f-222">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="2183f-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2183f-223">Search-Flags</span></span>           | <span data-ttu-id="2183f-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2183f-224">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="2183f-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2183f-225">System-Flags</span></span>           | <span data-ttu-id="2183f-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2183f-226">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="2183f-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2183f-227">Classes used in</span></span>        | [<span data-ttu-id="2183f-228">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2183f-228">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="2183f-229">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2183f-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2183f-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2183f-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2183f-231">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2183f-231">Entry</span></span> | <span data-ttu-id="2183f-232">Wert</span><span class="sxs-lookup"><span data-stu-id="2183f-232">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2183f-233">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2183f-233">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2183f-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2183f-234">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2183f-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="2183f-235">System-Only</span></span>            | <span data-ttu-id="2183f-236">False</span><span class="sxs-lookup"><span data-stu-id="2183f-236">False</span></span>                                                                                         |
| <span data-ttu-id="2183f-237">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2183f-237">Is-Single-Valued</span></span>       | <span data-ttu-id="2183f-238">Richtig</span><span class="sxs-lookup"><span data-stu-id="2183f-238">True</span></span>                                                                                          |
| <span data-ttu-id="2183f-239">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2183f-239">Is Indexed</span></span>             | <span data-ttu-id="2183f-240">False</span><span class="sxs-lookup"><span data-stu-id="2183f-240">False</span></span>                                                                                         |
| <span data-ttu-id="2183f-241">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2183f-241">In Global Catalog</span></span>      | <span data-ttu-id="2183f-242">Richtig</span><span class="sxs-lookup"><span data-stu-id="2183f-242">True</span></span>                                                                                          |
| <span data-ttu-id="2183f-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2183f-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="2183f-244">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2183f-244">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="2183f-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2183f-245">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="2183f-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2183f-246">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="2183f-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2183f-247">Search-Flags</span></span>           | <span data-ttu-id="2183f-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2183f-248">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="2183f-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2183f-249">System-Flags</span></span>           | <span data-ttu-id="2183f-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2183f-250">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="2183f-251">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2183f-251">Classes used in</span></span>        | [<span data-ttu-id="2183f-252">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2183f-252">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="2183f-253">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2183f-253">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2183f-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2183f-254">Windows Server 2012</span></span>



| <span data-ttu-id="2183f-255">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2183f-255">Entry</span></span> | <span data-ttu-id="2183f-256">Wert</span><span class="sxs-lookup"><span data-stu-id="2183f-256">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2183f-257">Link-ID</span><span class="sxs-lookup"><span data-stu-id="2183f-257">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2183f-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2183f-258">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2183f-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="2183f-259">System-Only</span></span>            | <span data-ttu-id="2183f-260">False</span><span class="sxs-lookup"><span data-stu-id="2183f-260">False</span></span>                                                                                         |
| <span data-ttu-id="2183f-261">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="2183f-261">Is-Single-Valued</span></span>       | <span data-ttu-id="2183f-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="2183f-262">True</span></span>                                                                                          |
| <span data-ttu-id="2183f-263">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="2183f-263">Is Indexed</span></span>             | <span data-ttu-id="2183f-264">False</span><span class="sxs-lookup"><span data-stu-id="2183f-264">False</span></span>                                                                                         |
| <span data-ttu-id="2183f-265">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="2183f-265">In Global Catalog</span></span>      | <span data-ttu-id="2183f-266">Richtig</span><span class="sxs-lookup"><span data-stu-id="2183f-266">True</span></span>                                                                                          |
| <span data-ttu-id="2183f-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2183f-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="2183f-268">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="2183f-268">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="2183f-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2183f-269">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="2183f-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2183f-270">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="2183f-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2183f-271">Search-Flags</span></span>           | <span data-ttu-id="2183f-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2183f-272">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="2183f-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2183f-273">System-Flags</span></span>           | <span data-ttu-id="2183f-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2183f-274">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="2183f-275">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="2183f-275">Classes used in</span></span>        | [<span data-ttu-id="2183f-276">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2183f-276">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="2183f-277">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="2183f-277">**User**</span></span>](c-user.md)<br/> |



 

 





