---
title: Link-Track-Secret-Attribut
description: Dieses Attribut speichert einen Link zu einem geheimen Schlüssel, mit dem eine verschlüsselte Datei in Klartext übersetzt werden kann.
ms.assetid: e476f4af-71a8-4bd9-a81d-f825bfbf267b
ms.tgt_platform: multiple
keywords:
- AD-Schema für Link-Track-Secret-Attribut
- linktracksecret-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Link-Track-Secret
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb172ec0985acc7c93c62796881c369c7ad0b82
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106343080"
---
# <a name="link-track-secret-attribute"></a><span data-ttu-id="8292b-105">Link-Track-Secret-Attribut</span><span class="sxs-lookup"><span data-stu-id="8292b-105">Link-Track-Secret attribute</span></span>

<span data-ttu-id="8292b-106">Dieses Attribut speichert einen Link zu einem geheimen Schlüssel, mit dem eine verschlüsselte Datei in Klartext übersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8292b-106">This attribute stores a link to a secret key that allows an encrypted file to be translated to plaintext.</span></span>



| <span data-ttu-id="8292b-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8292b-107">Entry</span></span> | <span data-ttu-id="8292b-108">Wert</span><span class="sxs-lookup"><span data-stu-id="8292b-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="8292b-109">CN</span><span class="sxs-lookup"><span data-stu-id="8292b-109">CN</span></span>                | <span data-ttu-id="8292b-110">Link-Track-Secret</span><span class="sxs-lookup"><span data-stu-id="8292b-110">Link-Track-Secret</span></span>                                     |
| <span data-ttu-id="8292b-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8292b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8292b-112">linktracksecret</span><span class="sxs-lookup"><span data-stu-id="8292b-112">linkTrackSecret</span></span>                                       |
| <span data-ttu-id="8292b-113">Size</span><span class="sxs-lookup"><span data-stu-id="8292b-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="8292b-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="8292b-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="8292b-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="8292b-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="8292b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8292b-116">Attribute-Id</span></span>      | <span data-ttu-id="8292b-117">1.2.840.113556.1.4.269</span><span class="sxs-lookup"><span data-stu-id="8292b-117">1.2.840.113556.1.4.269</span></span>                                |
| <span data-ttu-id="8292b-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8292b-118">System-Id-Guid</span></span>    | <span data-ttu-id="8292b-119">2ae80fe2-47b4-11D0-a1a4-00c04f 930c9</span><span class="sxs-lookup"><span data-stu-id="8292b-119">2ae80fe2-47b4-11d0-a1a4-00c04fd930c9</span></span>                  |
| <span data-ttu-id="8292b-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="8292b-120">Syntax</span></span>            | [<span data-ttu-id="8292b-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="8292b-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="8292b-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="8292b-122">Implementations</span></span>

-   [<span data-ttu-id="8292b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8292b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8292b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8292b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8292b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8292b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8292b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8292b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8292b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8292b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8292b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8292b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8292b-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8292b-129">Windows 2000 Server</span></span>



| <span data-ttu-id="8292b-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8292b-130">Entry</span></span> | <span data-ttu-id="8292b-131">Wert</span><span class="sxs-lookup"><span data-stu-id="8292b-131">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="8292b-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8292b-132">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="8292b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8292b-133">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="8292b-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="8292b-134">System-Only</span></span>            | <span data-ttu-id="8292b-135">False</span><span class="sxs-lookup"><span data-stu-id="8292b-135">False</span></span>                                                          |
| <span data-ttu-id="8292b-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8292b-136">Is-Single-Valued</span></span>       | <span data-ttu-id="8292b-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="8292b-137">True</span></span>                                                           |
| <span data-ttu-id="8292b-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8292b-138">Is Indexed</span></span>             | <span data-ttu-id="8292b-139">False</span><span class="sxs-lookup"><span data-stu-id="8292b-139">False</span></span>                                                          |
| <span data-ttu-id="8292b-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8292b-140">In Global Catalog</span></span>      | <span data-ttu-id="8292b-141">False</span><span class="sxs-lookup"><span data-stu-id="8292b-141">False</span></span>                                                          |
| <span data-ttu-id="8292b-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8292b-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="8292b-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8292b-143">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="8292b-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8292b-144">Range-Lower</span></span>            | <span data-ttu-id="8292b-145">0</span><span class="sxs-lookup"><span data-stu-id="8292b-145">0</span></span>                                                              |
| <span data-ttu-id="8292b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8292b-146">Range-Upper</span></span>            | <span data-ttu-id="8292b-147">16</span><span class="sxs-lookup"><span data-stu-id="8292b-147">16</span></span>                                                             |
| <span data-ttu-id="8292b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8292b-148">Search-Flags</span></span>           | <span data-ttu-id="8292b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8292b-149">0x00000000</span></span>                                                     |
| <span data-ttu-id="8292b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8292b-150">System-Flags</span></span>           | <span data-ttu-id="8292b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8292b-151">0x00000010</span></span>                                                     |
| <span data-ttu-id="8292b-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8292b-152">Classes used in</span></span>        | [<span data-ttu-id="8292b-153">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="8292b-153">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8292b-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8292b-154">Windows Server 2003</span></span>



| <span data-ttu-id="8292b-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8292b-155">Entry</span></span> | <span data-ttu-id="8292b-156">Wert</span><span class="sxs-lookup"><span data-stu-id="8292b-156">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="8292b-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8292b-157">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="8292b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8292b-158">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="8292b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="8292b-159">System-Only</span></span>            | <span data-ttu-id="8292b-160">False</span><span class="sxs-lookup"><span data-stu-id="8292b-160">False</span></span>                                                          |
| <span data-ttu-id="8292b-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8292b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="8292b-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="8292b-162">True</span></span>                                                           |
| <span data-ttu-id="8292b-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8292b-163">Is Indexed</span></span>             | <span data-ttu-id="8292b-164">False</span><span class="sxs-lookup"><span data-stu-id="8292b-164">False</span></span>                                                          |
| <span data-ttu-id="8292b-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8292b-165">In Global Catalog</span></span>      | <span data-ttu-id="8292b-166">False</span><span class="sxs-lookup"><span data-stu-id="8292b-166">False</span></span>                                                          |
| <span data-ttu-id="8292b-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8292b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="8292b-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8292b-168">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="8292b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8292b-169">Range-Lower</span></span>            | <span data-ttu-id="8292b-170">0</span><span class="sxs-lookup"><span data-stu-id="8292b-170">0</span></span>                                                              |
| <span data-ttu-id="8292b-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8292b-171">Range-Upper</span></span>            | <span data-ttu-id="8292b-172">16</span><span class="sxs-lookup"><span data-stu-id="8292b-172">16</span></span>                                                             |
| <span data-ttu-id="8292b-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8292b-173">Search-Flags</span></span>           | <span data-ttu-id="8292b-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8292b-174">0x00000000</span></span>                                                     |
| <span data-ttu-id="8292b-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8292b-175">System-Flags</span></span>           | <span data-ttu-id="8292b-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8292b-176">0x00000010</span></span>                                                     |
| <span data-ttu-id="8292b-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8292b-177">Classes used in</span></span>        | [<span data-ttu-id="8292b-178">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="8292b-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8292b-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8292b-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8292b-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8292b-180">Entry</span></span> | <span data-ttu-id="8292b-181">Wert</span><span class="sxs-lookup"><span data-stu-id="8292b-181">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="8292b-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8292b-182">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="8292b-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8292b-183">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="8292b-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="8292b-184">System-Only</span></span>            | <span data-ttu-id="8292b-185">False</span><span class="sxs-lookup"><span data-stu-id="8292b-185">False</span></span>                                                          |
| <span data-ttu-id="8292b-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8292b-186">Is-Single-Valued</span></span>       | <span data-ttu-id="8292b-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="8292b-187">True</span></span>                                                           |
| <span data-ttu-id="8292b-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8292b-188">Is Indexed</span></span>             | <span data-ttu-id="8292b-189">False</span><span class="sxs-lookup"><span data-stu-id="8292b-189">False</span></span>                                                          |
| <span data-ttu-id="8292b-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8292b-190">In Global Catalog</span></span>      | <span data-ttu-id="8292b-191">False</span><span class="sxs-lookup"><span data-stu-id="8292b-191">False</span></span>                                                          |
| <span data-ttu-id="8292b-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8292b-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="8292b-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8292b-193">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="8292b-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8292b-194">Range-Lower</span></span>            | <span data-ttu-id="8292b-195">0</span><span class="sxs-lookup"><span data-stu-id="8292b-195">0</span></span>                                                              |
| <span data-ttu-id="8292b-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8292b-196">Range-Upper</span></span>            | <span data-ttu-id="8292b-197">16</span><span class="sxs-lookup"><span data-stu-id="8292b-197">16</span></span>                                                             |
| <span data-ttu-id="8292b-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8292b-198">Search-Flags</span></span>           | <span data-ttu-id="8292b-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8292b-199">0x00000000</span></span>                                                     |
| <span data-ttu-id="8292b-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8292b-200">System-Flags</span></span>           | <span data-ttu-id="8292b-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8292b-201">0x00000010</span></span>                                                     |
| <span data-ttu-id="8292b-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8292b-202">Classes used in</span></span>        | [<span data-ttu-id="8292b-203">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="8292b-203">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8292b-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8292b-204">Windows Server 2008</span></span>



| <span data-ttu-id="8292b-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8292b-205">Entry</span></span> | <span data-ttu-id="8292b-206">Wert</span><span class="sxs-lookup"><span data-stu-id="8292b-206">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="8292b-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8292b-207">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="8292b-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8292b-208">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="8292b-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="8292b-209">System-Only</span></span>            | <span data-ttu-id="8292b-210">False</span><span class="sxs-lookup"><span data-stu-id="8292b-210">False</span></span>                                                          |
| <span data-ttu-id="8292b-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8292b-211">Is-Single-Valued</span></span>       | <span data-ttu-id="8292b-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="8292b-212">True</span></span>                                                           |
| <span data-ttu-id="8292b-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8292b-213">Is Indexed</span></span>             | <span data-ttu-id="8292b-214">False</span><span class="sxs-lookup"><span data-stu-id="8292b-214">False</span></span>                                                          |
| <span data-ttu-id="8292b-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8292b-215">In Global Catalog</span></span>      | <span data-ttu-id="8292b-216">False</span><span class="sxs-lookup"><span data-stu-id="8292b-216">False</span></span>                                                          |
| <span data-ttu-id="8292b-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8292b-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="8292b-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8292b-218">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="8292b-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8292b-219">Range-Lower</span></span>            | <span data-ttu-id="8292b-220">0</span><span class="sxs-lookup"><span data-stu-id="8292b-220">0</span></span>                                                              |
| <span data-ttu-id="8292b-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8292b-221">Range-Upper</span></span>            | <span data-ttu-id="8292b-222">16</span><span class="sxs-lookup"><span data-stu-id="8292b-222">16</span></span>                                                             |
| <span data-ttu-id="8292b-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8292b-223">Search-Flags</span></span>           | <span data-ttu-id="8292b-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8292b-224">0x00000000</span></span>                                                     |
| <span data-ttu-id="8292b-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8292b-225">System-Flags</span></span>           | <span data-ttu-id="8292b-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8292b-226">0x00000010</span></span>                                                     |
| <span data-ttu-id="8292b-227">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8292b-227">Classes used in</span></span>        | [<span data-ttu-id="8292b-228">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="8292b-228">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8292b-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8292b-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8292b-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8292b-230">Entry</span></span> | <span data-ttu-id="8292b-231">Wert</span><span class="sxs-lookup"><span data-stu-id="8292b-231">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="8292b-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8292b-232">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="8292b-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8292b-233">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="8292b-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="8292b-234">System-Only</span></span>            | <span data-ttu-id="8292b-235">False</span><span class="sxs-lookup"><span data-stu-id="8292b-235">False</span></span>                                                          |
| <span data-ttu-id="8292b-236">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8292b-236">Is-Single-Valued</span></span>       | <span data-ttu-id="8292b-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="8292b-237">True</span></span>                                                           |
| <span data-ttu-id="8292b-238">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8292b-238">Is Indexed</span></span>             | <span data-ttu-id="8292b-239">False</span><span class="sxs-lookup"><span data-stu-id="8292b-239">False</span></span>                                                          |
| <span data-ttu-id="8292b-240">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8292b-240">In Global Catalog</span></span>      | <span data-ttu-id="8292b-241">False</span><span class="sxs-lookup"><span data-stu-id="8292b-241">False</span></span>                                                          |
| <span data-ttu-id="8292b-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8292b-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="8292b-243">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8292b-243">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="8292b-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8292b-244">Range-Lower</span></span>            | <span data-ttu-id="8292b-245">0</span><span class="sxs-lookup"><span data-stu-id="8292b-245">0</span></span>                                                              |
| <span data-ttu-id="8292b-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8292b-246">Range-Upper</span></span>            | <span data-ttu-id="8292b-247">16</span><span class="sxs-lookup"><span data-stu-id="8292b-247">16</span></span>                                                             |
| <span data-ttu-id="8292b-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8292b-248">Search-Flags</span></span>           | <span data-ttu-id="8292b-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8292b-249">0x00000000</span></span>                                                     |
| <span data-ttu-id="8292b-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8292b-250">System-Flags</span></span>           | <span data-ttu-id="8292b-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8292b-251">0x00000010</span></span>                                                     |
| <span data-ttu-id="8292b-252">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8292b-252">Classes used in</span></span>        | [<span data-ttu-id="8292b-253">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="8292b-253">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8292b-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8292b-254">Windows Server 2012</span></span>



| <span data-ttu-id="8292b-255">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8292b-255">Entry</span></span> | <span data-ttu-id="8292b-256">Wert</span><span class="sxs-lookup"><span data-stu-id="8292b-256">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="8292b-257">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8292b-257">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="8292b-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8292b-258">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="8292b-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="8292b-259">System-Only</span></span>            | <span data-ttu-id="8292b-260">False</span><span class="sxs-lookup"><span data-stu-id="8292b-260">False</span></span>                                                          |
| <span data-ttu-id="8292b-261">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8292b-261">Is-Single-Valued</span></span>       | <span data-ttu-id="8292b-262">Richtig</span><span class="sxs-lookup"><span data-stu-id="8292b-262">True</span></span>                                                           |
| <span data-ttu-id="8292b-263">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8292b-263">Is Indexed</span></span>             | <span data-ttu-id="8292b-264">False</span><span class="sxs-lookup"><span data-stu-id="8292b-264">False</span></span>                                                          |
| <span data-ttu-id="8292b-265">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8292b-265">In Global Catalog</span></span>      | <span data-ttu-id="8292b-266">False</span><span class="sxs-lookup"><span data-stu-id="8292b-266">False</span></span>                                                          |
| <span data-ttu-id="8292b-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8292b-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="8292b-268">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8292b-268">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="8292b-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8292b-269">Range-Lower</span></span>            | <span data-ttu-id="8292b-270">0</span><span class="sxs-lookup"><span data-stu-id="8292b-270">0</span></span>                                                              |
| <span data-ttu-id="8292b-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8292b-271">Range-Upper</span></span>            | <span data-ttu-id="8292b-272">16</span><span class="sxs-lookup"><span data-stu-id="8292b-272">16</span></span>                                                             |
| <span data-ttu-id="8292b-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8292b-273">Search-Flags</span></span>           | <span data-ttu-id="8292b-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8292b-274">0x00000000</span></span>                                                     |
| <span data-ttu-id="8292b-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8292b-275">System-Flags</span></span>           | <span data-ttu-id="8292b-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8292b-276">0x00000010</span></span>                                                     |
| <span data-ttu-id="8292b-277">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8292b-277">Classes used in</span></span>        | [<span data-ttu-id="8292b-278">**Link-Track-Vol-Entry**</span><span class="sxs-lookup"><span data-stu-id="8292b-278">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





