---
title: MSMQ-Digests-Attribut
description: Ein Array von Digests der entsprechenden Zertifikate in Attribut MSMQ-Sign-Zertifikats. Sie werden für die Zuordnung eines Digest zu einem Zertifikat verwendet.
ms.assetid: a9b03edd-1506-4f2d-afe1-7d953977f6fa
ms.tgt_platform: multiple
keywords:
- AD-Schema für MSMQ-Digests-Attribut
- AD-Schema des msmqdigests-Attributs
topic_type:
- apiref
api_name:
- MSMQ-Digests
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d51c607b1d99af0aed46f259513f4bcf790844
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344900"
---
# <a name="msmq-digests-attribute"></a><span data-ttu-id="19f32-106">MSMQ-Digests-Attribut</span><span class="sxs-lookup"><span data-stu-id="19f32-106">MSMQ-Digests attribute</span></span>

<span data-ttu-id="19f32-107">Ein Array von Digests der entsprechenden Zertifikate in Attribut MSMQ-Sign-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="19f32-107">An array of digests of the corresponding certificates in attribute mSMQ-Sign-Certificates.</span></span> <span data-ttu-id="19f32-108">Sie werden für die Zuordnung eines Digest zu einem Zertifikat verwendet.</span><span class="sxs-lookup"><span data-stu-id="19f32-108">They are used for mapping a digest into a certificate.</span></span>



| <span data-ttu-id="19f32-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="19f32-109">Entry</span></span> | <span data-ttu-id="19f32-110">Wert</span><span class="sxs-lookup"><span data-stu-id="19f32-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="19f32-111">CN</span><span class="sxs-lookup"><span data-stu-id="19f32-111">CN</span></span>                | <span data-ttu-id="19f32-112">MSMQ-Digests</span><span class="sxs-lookup"><span data-stu-id="19f32-112">MSMQ-Digests</span></span>                                          |
| <span data-ttu-id="19f32-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="19f32-113">Ldap-Display-Name</span></span> | <span data-ttu-id="19f32-114">msmqdigests</span><span class="sxs-lookup"><span data-stu-id="19f32-114">mSMQDigests</span></span>                                           |
| <span data-ttu-id="19f32-115">Size</span><span class="sxs-lookup"><span data-stu-id="19f32-115">Size</span></span>              | <span data-ttu-id="19f32-116">Jeder Digest ist 16 Bytes.</span><span class="sxs-lookup"><span data-stu-id="19f32-116">Each digest is 16 bytes.</span></span>                              |
| <span data-ttu-id="19f32-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="19f32-117">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="19f32-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="19f32-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="19f32-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="19f32-119">Attribute-Id</span></span>      | <span data-ttu-id="19f32-120">1.2.840.113556.1.4.948</span><span class="sxs-lookup"><span data-stu-id="19f32-120">1.2.840.113556.1.4.948</span></span>                                |
| <span data-ttu-id="19f32-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="19f32-121">System-Id-Guid</span></span>    | <span data-ttu-id="19f32-122">9a0dc33c-C100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="19f32-122">9a0dc33c-c100-11d1-bbc5-0080c76670c0</span></span>                  |
| <span data-ttu-id="19f32-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="19f32-123">Syntax</span></span>            | [<span data-ttu-id="19f32-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="19f32-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="19f32-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="19f32-125">Implementations</span></span>

-   [<span data-ttu-id="19f32-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="19f32-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="19f32-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="19f32-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="19f32-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="19f32-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="19f32-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="19f32-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="19f32-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="19f32-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="19f32-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="19f32-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="19f32-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="19f32-132">Windows 2000 Server</span></span>



| <span data-ttu-id="19f32-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="19f32-133">Entry</span></span> | <span data-ttu-id="19f32-134">Wert</span><span class="sxs-lookup"><span data-stu-id="19f32-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="19f32-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="19f32-135">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="19f32-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f32-136">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="19f32-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f32-137">System-Only</span></span>            | <span data-ttu-id="19f32-138">False</span><span class="sxs-lookup"><span data-stu-id="19f32-138">False</span></span>                                                                                         |
| <span data-ttu-id="19f32-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="19f32-139">Is-Single-Valued</span></span>       | <span data-ttu-id="19f32-140">False</span><span class="sxs-lookup"><span data-stu-id="19f32-140">False</span></span>                                                                                         |
| <span data-ttu-id="19f32-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="19f32-141">Is Indexed</span></span>             | <span data-ttu-id="19f32-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="19f32-142">True</span></span>                                                                                          |
| <span data-ttu-id="19f32-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="19f32-143">In Global Catalog</span></span>      | <span data-ttu-id="19f32-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="19f32-144">True</span></span>                                                                                          |
| <span data-ttu-id="19f32-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19f32-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f32-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="19f32-146">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="19f32-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f32-147">Range-Lower</span></span>            | <span data-ttu-id="19f32-148">16</span><span class="sxs-lookup"><span data-stu-id="19f32-148">16</span></span>                                                                                            |
| <span data-ttu-id="19f32-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f32-149">Range-Upper</span></span>            | <span data-ttu-id="19f32-150">16</span><span class="sxs-lookup"><span data-stu-id="19f32-150">16</span></span>                                                                                            |
| <span data-ttu-id="19f32-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f32-151">Search-Flags</span></span>           | <span data-ttu-id="19f32-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="19f32-152">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="19f32-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f32-153">System-Flags</span></span>           | <span data-ttu-id="19f32-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f32-154">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="19f32-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="19f32-155">Classes used in</span></span>        | [<span data-ttu-id="19f32-156">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="19f32-156">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="19f32-157">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="19f32-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="19f32-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="19f32-158">Windows Server 2003</span></span>



| <span data-ttu-id="19f32-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="19f32-159">Entry</span></span> | <span data-ttu-id="19f32-160">Wert</span><span class="sxs-lookup"><span data-stu-id="19f32-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="19f32-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="19f32-161">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="19f32-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f32-162">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="19f32-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f32-163">System-Only</span></span>            | <span data-ttu-id="19f32-164">False</span><span class="sxs-lookup"><span data-stu-id="19f32-164">False</span></span>                                                                                         |
| <span data-ttu-id="19f32-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="19f32-165">Is-Single-Valued</span></span>       | <span data-ttu-id="19f32-166">False</span><span class="sxs-lookup"><span data-stu-id="19f32-166">False</span></span>                                                                                         |
| <span data-ttu-id="19f32-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="19f32-167">Is Indexed</span></span>             | <span data-ttu-id="19f32-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="19f32-168">True</span></span>                                                                                          |
| <span data-ttu-id="19f32-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="19f32-169">In Global Catalog</span></span>      | <span data-ttu-id="19f32-170">Richtig</span><span class="sxs-lookup"><span data-stu-id="19f32-170">True</span></span>                                                                                          |
| <span data-ttu-id="19f32-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19f32-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f32-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="19f32-172">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="19f32-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f32-173">Range-Lower</span></span>            | <span data-ttu-id="19f32-174">16</span><span class="sxs-lookup"><span data-stu-id="19f32-174">16</span></span>                                                                                            |
| <span data-ttu-id="19f32-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f32-175">Range-Upper</span></span>            | <span data-ttu-id="19f32-176">16</span><span class="sxs-lookup"><span data-stu-id="19f32-176">16</span></span>                                                                                            |
| <span data-ttu-id="19f32-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f32-177">Search-Flags</span></span>           | <span data-ttu-id="19f32-178">0x00000001</span><span class="sxs-lookup"><span data-stu-id="19f32-178">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="19f32-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f32-179">System-Flags</span></span>           | <span data-ttu-id="19f32-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f32-180">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="19f32-181">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="19f32-181">Classes used in</span></span>        | [<span data-ttu-id="19f32-182">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="19f32-182">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="19f32-183">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="19f32-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="19f32-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="19f32-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="19f32-185">Eingabe</span><span class="sxs-lookup"><span data-stu-id="19f32-185">Entry</span></span> | <span data-ttu-id="19f32-186">Wert</span><span class="sxs-lookup"><span data-stu-id="19f32-186">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="19f32-187">Link-ID</span><span class="sxs-lookup"><span data-stu-id="19f32-187">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="19f32-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f32-188">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="19f32-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f32-189">System-Only</span></span>            | <span data-ttu-id="19f32-190">False</span><span class="sxs-lookup"><span data-stu-id="19f32-190">False</span></span>                                                                                         |
| <span data-ttu-id="19f32-191">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="19f32-191">Is-Single-Valued</span></span>       | <span data-ttu-id="19f32-192">False</span><span class="sxs-lookup"><span data-stu-id="19f32-192">False</span></span>                                                                                         |
| <span data-ttu-id="19f32-193">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="19f32-193">Is Indexed</span></span>             | <span data-ttu-id="19f32-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="19f32-194">True</span></span>                                                                                          |
| <span data-ttu-id="19f32-195">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="19f32-195">In Global Catalog</span></span>      | <span data-ttu-id="19f32-196">Richtig</span><span class="sxs-lookup"><span data-stu-id="19f32-196">True</span></span>                                                                                          |
| <span data-ttu-id="19f32-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19f32-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f32-198">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="19f32-198">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="19f32-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f32-199">Range-Lower</span></span>            | <span data-ttu-id="19f32-200">16</span><span class="sxs-lookup"><span data-stu-id="19f32-200">16</span></span>                                                                                            |
| <span data-ttu-id="19f32-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f32-201">Range-Upper</span></span>            | <span data-ttu-id="19f32-202">16</span><span class="sxs-lookup"><span data-stu-id="19f32-202">16</span></span>                                                                                            |
| <span data-ttu-id="19f32-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f32-203">Search-Flags</span></span>           | <span data-ttu-id="19f32-204">0x00000001</span><span class="sxs-lookup"><span data-stu-id="19f32-204">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="19f32-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f32-205">System-Flags</span></span>           | <span data-ttu-id="19f32-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f32-206">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="19f32-207">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="19f32-207">Classes used in</span></span>        | [<span data-ttu-id="19f32-208">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="19f32-208">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="19f32-209">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="19f32-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="19f32-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19f32-210">Windows Server 2008</span></span>



| <span data-ttu-id="19f32-211">Eingabe</span><span class="sxs-lookup"><span data-stu-id="19f32-211">Entry</span></span> | <span data-ttu-id="19f32-212">Wert</span><span class="sxs-lookup"><span data-stu-id="19f32-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="19f32-213">Link-ID</span><span class="sxs-lookup"><span data-stu-id="19f32-213">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="19f32-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f32-214">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="19f32-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f32-215">System-Only</span></span>            | <span data-ttu-id="19f32-216">False</span><span class="sxs-lookup"><span data-stu-id="19f32-216">False</span></span>                                                                                         |
| <span data-ttu-id="19f32-217">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="19f32-217">Is-Single-Valued</span></span>       | <span data-ttu-id="19f32-218">False</span><span class="sxs-lookup"><span data-stu-id="19f32-218">False</span></span>                                                                                         |
| <span data-ttu-id="19f32-219">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="19f32-219">Is Indexed</span></span>             | <span data-ttu-id="19f32-220">Richtig</span><span class="sxs-lookup"><span data-stu-id="19f32-220">True</span></span>                                                                                          |
| <span data-ttu-id="19f32-221">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="19f32-221">In Global Catalog</span></span>      | <span data-ttu-id="19f32-222">Richtig</span><span class="sxs-lookup"><span data-stu-id="19f32-222">True</span></span>                                                                                          |
| <span data-ttu-id="19f32-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19f32-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f32-224">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="19f32-224">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="19f32-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f32-225">Range-Lower</span></span>            | <span data-ttu-id="19f32-226">16</span><span class="sxs-lookup"><span data-stu-id="19f32-226">16</span></span>                                                                                            |
| <span data-ttu-id="19f32-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f32-227">Range-Upper</span></span>            | <span data-ttu-id="19f32-228">16</span><span class="sxs-lookup"><span data-stu-id="19f32-228">16</span></span>                                                                                            |
| <span data-ttu-id="19f32-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f32-229">Search-Flags</span></span>           | <span data-ttu-id="19f32-230">0x00000001</span><span class="sxs-lookup"><span data-stu-id="19f32-230">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="19f32-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f32-231">System-Flags</span></span>           | <span data-ttu-id="19f32-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f32-232">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="19f32-233">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="19f32-233">Classes used in</span></span>        | [<span data-ttu-id="19f32-234">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="19f32-234">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="19f32-235">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="19f32-235">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="19f32-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="19f32-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="19f32-237">Eingabe</span><span class="sxs-lookup"><span data-stu-id="19f32-237">Entry</span></span> | <span data-ttu-id="19f32-238">Wert</span><span class="sxs-lookup"><span data-stu-id="19f32-238">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="19f32-239">Link-ID</span><span class="sxs-lookup"><span data-stu-id="19f32-239">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="19f32-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f32-240">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="19f32-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f32-241">System-Only</span></span>            | <span data-ttu-id="19f32-242">False</span><span class="sxs-lookup"><span data-stu-id="19f32-242">False</span></span>                                                                                         |
| <span data-ttu-id="19f32-243">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="19f32-243">Is-Single-Valued</span></span>       | <span data-ttu-id="19f32-244">False</span><span class="sxs-lookup"><span data-stu-id="19f32-244">False</span></span>                                                                                         |
| <span data-ttu-id="19f32-245">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="19f32-245">Is Indexed</span></span>             | <span data-ttu-id="19f32-246">Richtig</span><span class="sxs-lookup"><span data-stu-id="19f32-246">True</span></span>                                                                                          |
| <span data-ttu-id="19f32-247">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="19f32-247">In Global Catalog</span></span>      | <span data-ttu-id="19f32-248">Richtig</span><span class="sxs-lookup"><span data-stu-id="19f32-248">True</span></span>                                                                                          |
| <span data-ttu-id="19f32-249">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19f32-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f32-250">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="19f32-250">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="19f32-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f32-251">Range-Lower</span></span>            | <span data-ttu-id="19f32-252">16</span><span class="sxs-lookup"><span data-stu-id="19f32-252">16</span></span>                                                                                            |
| <span data-ttu-id="19f32-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f32-253">Range-Upper</span></span>            | <span data-ttu-id="19f32-254">16</span><span class="sxs-lookup"><span data-stu-id="19f32-254">16</span></span>                                                                                            |
| <span data-ttu-id="19f32-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f32-255">Search-Flags</span></span>           | <span data-ttu-id="19f32-256">0x00000001</span><span class="sxs-lookup"><span data-stu-id="19f32-256">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="19f32-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f32-257">System-Flags</span></span>           | <span data-ttu-id="19f32-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f32-258">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="19f32-259">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="19f32-259">Classes used in</span></span>        | [<span data-ttu-id="19f32-260">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="19f32-260">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="19f32-261">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="19f32-261">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="19f32-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="19f32-262">Windows Server 2012</span></span>



| <span data-ttu-id="19f32-263">Eingabe</span><span class="sxs-lookup"><span data-stu-id="19f32-263">Entry</span></span> | <span data-ttu-id="19f32-264">Wert</span><span class="sxs-lookup"><span data-stu-id="19f32-264">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="19f32-265">Link-ID</span><span class="sxs-lookup"><span data-stu-id="19f32-265">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="19f32-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19f32-266">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="19f32-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="19f32-267">System-Only</span></span>            | <span data-ttu-id="19f32-268">False</span><span class="sxs-lookup"><span data-stu-id="19f32-268">False</span></span>                                                                                         |
| <span data-ttu-id="19f32-269">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="19f32-269">Is-Single-Valued</span></span>       | <span data-ttu-id="19f32-270">False</span><span class="sxs-lookup"><span data-stu-id="19f32-270">False</span></span>                                                                                         |
| <span data-ttu-id="19f32-271">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="19f32-271">Is Indexed</span></span>             | <span data-ttu-id="19f32-272">Richtig</span><span class="sxs-lookup"><span data-stu-id="19f32-272">True</span></span>                                                                                          |
| <span data-ttu-id="19f32-273">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="19f32-273">In Global Catalog</span></span>      | <span data-ttu-id="19f32-274">Richtig</span><span class="sxs-lookup"><span data-stu-id="19f32-274">True</span></span>                                                                                          |
| <span data-ttu-id="19f32-275">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="19f32-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="19f32-276">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="19f32-276">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="19f32-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19f32-277">Range-Lower</span></span>            | <span data-ttu-id="19f32-278">16</span><span class="sxs-lookup"><span data-stu-id="19f32-278">16</span></span>                                                                                            |
| <span data-ttu-id="19f32-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19f32-279">Range-Upper</span></span>            | <span data-ttu-id="19f32-280">16</span><span class="sxs-lookup"><span data-stu-id="19f32-280">16</span></span>                                                                                            |
| <span data-ttu-id="19f32-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19f32-281">Search-Flags</span></span>           | <span data-ttu-id="19f32-282">0x00000001</span><span class="sxs-lookup"><span data-stu-id="19f32-282">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="19f32-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19f32-283">System-Flags</span></span>           | <span data-ttu-id="19f32-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19f32-284">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="19f32-285">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="19f32-285">Classes used in</span></span>        | [<span data-ttu-id="19f32-286">**MSMQ-migriert-Benutzer**</span><span class="sxs-lookup"><span data-stu-id="19f32-286">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="19f32-287">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="19f32-287">**User**</span></span>](c-user.md)<br/> |



 

 





