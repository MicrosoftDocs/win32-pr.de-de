---
title: Last-Update-Sequence-Attribut
description: Dieses Attribut enthält die Aktualisierungs Sequenznummer für das letzte Element im Klassen Speicher, das geändert wurde.
ms.assetid: fd434b8d-31b4-45f7-8d8f-048f61cabb92
ms.tgt_platform: multiple
keywords:
- AD-Schema des Last-Update-Sequence-Attributs
- lastupdatesequence-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Last-Update-Sequence
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e670c6784ded96a1e81d98f5f1c9bfb859efaa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346147"
---
# <a name="last-update-sequence-attribute"></a><span data-ttu-id="f67e7-105">Last-Update-Sequence-Attribut</span><span class="sxs-lookup"><span data-stu-id="f67e7-105">Last-Update-Sequence attribute</span></span>

<span data-ttu-id="f67e7-106">Dieses Attribut enthält die Aktualisierungs Sequenznummer für das letzte Element im Klassen Speicher, das geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f67e7-106">This attribute contains the update sequence number for the last item in the class store that was changed.</span></span>



| <span data-ttu-id="f67e7-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f67e7-107">Entry</span></span> | <span data-ttu-id="f67e7-108">Wert</span><span class="sxs-lookup"><span data-stu-id="f67e7-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f67e7-109">CN</span><span class="sxs-lookup"><span data-stu-id="f67e7-109">CN</span></span>                | <span data-ttu-id="f67e7-110">Letzte Update-Sequenz</span><span class="sxs-lookup"><span data-stu-id="f67e7-110">Last-Update-Sequence</span></span>                        |
| <span data-ttu-id="f67e7-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f67e7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f67e7-112">lastupdatesequence</span><span class="sxs-lookup"><span data-stu-id="f67e7-112">lastUpdateSequence</span></span>                          |
| <span data-ttu-id="f67e7-113">Size</span><span class="sxs-lookup"><span data-stu-id="f67e7-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="f67e7-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f67e7-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="f67e7-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f67e7-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="f67e7-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f67e7-116">Attribute-Id</span></span>      | <span data-ttu-id="f67e7-117">1.2.840.113556.1.4.330</span><span class="sxs-lookup"><span data-stu-id="f67e7-117">1.2.840.113556.1.4.330</span></span>                      |
| <span data-ttu-id="f67e7-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f67e7-118">System-Id-Guid</span></span>    | <span data-ttu-id="f67e7-119">7d6c0e9c-7E20-11D0-afd6-00c04 C9</span><span class="sxs-lookup"><span data-stu-id="f67e7-119">7d6c0e9c-7e20-11d0-afd6-00c04fd930c9</span></span>        |
| <span data-ttu-id="f67e7-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="f67e7-120">Syntax</span></span>            | [<span data-ttu-id="f67e7-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f67e7-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f67e7-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f67e7-122">Implementations</span></span>

-   [<span data-ttu-id="f67e7-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f67e7-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f67e7-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f67e7-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f67e7-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f67e7-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f67e7-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f67e7-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f67e7-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f67e7-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f67e7-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f67e7-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f67e7-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f67e7-129">Windows 2000 Server</span></span>



| <span data-ttu-id="f67e7-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f67e7-130">Entry</span></span> | <span data-ttu-id="f67e7-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f67e7-131">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f67e7-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f67e7-132">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f67e7-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f67e7-133">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f67e7-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f67e7-134">System-Only</span></span>            | <span data-ttu-id="f67e7-135">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-135">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f67e7-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f67e7-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="f67e7-137">True</span></span>                                                                                                            |
| <span data-ttu-id="f67e7-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f67e7-138">Is Indexed</span></span>             | <span data-ttu-id="f67e7-139">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-139">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f67e7-140">In Global Catalog</span></span>      | <span data-ttu-id="f67e7-141">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-141">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f67e7-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f67e7-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f67e7-143">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="f67e7-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f67e7-144">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f67e7-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f67e7-145">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f67e7-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f67e7-146">Search-Flags</span></span>           | <span data-ttu-id="f67e7-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f67e7-147">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="f67e7-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f67e7-148">System-Flags</span></span>           | <span data-ttu-id="f67e7-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f67e7-149">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="f67e7-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f67e7-150">Classes used in</span></span>        | [<span data-ttu-id="f67e7-151">**Class-Store**</span><span class="sxs-lookup"><span data-stu-id="f67e7-151">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="f67e7-152">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="f67e7-152">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f67e7-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f67e7-153">Windows Server 2003</span></span>



| <span data-ttu-id="f67e7-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f67e7-154">Entry</span></span> | <span data-ttu-id="f67e7-155">Wert</span><span class="sxs-lookup"><span data-stu-id="f67e7-155">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f67e7-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f67e7-156">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f67e7-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f67e7-157">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f67e7-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="f67e7-158">System-Only</span></span>            | <span data-ttu-id="f67e7-159">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-159">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f67e7-160">Is-Single-Valued</span></span>       | <span data-ttu-id="f67e7-161">Richtig</span><span class="sxs-lookup"><span data-stu-id="f67e7-161">True</span></span>                                                                                                            |
| <span data-ttu-id="f67e7-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f67e7-162">Is Indexed</span></span>             | <span data-ttu-id="f67e7-163">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-163">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f67e7-164">In Global Catalog</span></span>      | <span data-ttu-id="f67e7-165">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-165">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f67e7-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="f67e7-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f67e7-167">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="f67e7-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f67e7-168">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f67e7-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f67e7-169">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f67e7-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f67e7-170">Search-Flags</span></span>           | <span data-ttu-id="f67e7-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f67e7-171">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="f67e7-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f67e7-172">System-Flags</span></span>           | <span data-ttu-id="f67e7-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f67e7-173">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="f67e7-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f67e7-174">Classes used in</span></span>        | [<span data-ttu-id="f67e7-175">**Class-Store**</span><span class="sxs-lookup"><span data-stu-id="f67e7-175">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="f67e7-176">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="f67e7-176">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f67e7-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f67e7-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f67e7-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f67e7-178">Entry</span></span> | <span data-ttu-id="f67e7-179">Wert</span><span class="sxs-lookup"><span data-stu-id="f67e7-179">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f67e7-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f67e7-180">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f67e7-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f67e7-181">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f67e7-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="f67e7-182">System-Only</span></span>            | <span data-ttu-id="f67e7-183">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-183">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f67e7-184">Is-Single-Valued</span></span>       | <span data-ttu-id="f67e7-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="f67e7-185">True</span></span>                                                                                                            |
| <span data-ttu-id="f67e7-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f67e7-186">Is Indexed</span></span>             | <span data-ttu-id="f67e7-187">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-187">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f67e7-188">In Global Catalog</span></span>      | <span data-ttu-id="f67e7-189">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-189">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f67e7-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="f67e7-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f67e7-191">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="f67e7-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f67e7-192">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f67e7-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f67e7-193">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f67e7-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f67e7-194">Search-Flags</span></span>           | <span data-ttu-id="f67e7-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f67e7-195">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="f67e7-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f67e7-196">System-Flags</span></span>           | <span data-ttu-id="f67e7-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f67e7-197">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="f67e7-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f67e7-198">Classes used in</span></span>        | [<span data-ttu-id="f67e7-199">**Class-Store**</span><span class="sxs-lookup"><span data-stu-id="f67e7-199">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="f67e7-200">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="f67e7-200">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f67e7-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f67e7-201">Windows Server 2008</span></span>



| <span data-ttu-id="f67e7-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f67e7-202">Entry</span></span> | <span data-ttu-id="f67e7-203">Wert</span><span class="sxs-lookup"><span data-stu-id="f67e7-203">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f67e7-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f67e7-204">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f67e7-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f67e7-205">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f67e7-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="f67e7-206">System-Only</span></span>            | <span data-ttu-id="f67e7-207">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-207">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f67e7-208">Is-Single-Valued</span></span>       | <span data-ttu-id="f67e7-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="f67e7-209">True</span></span>                                                                                                            |
| <span data-ttu-id="f67e7-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f67e7-210">Is Indexed</span></span>             | <span data-ttu-id="f67e7-211">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-211">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f67e7-212">In Global Catalog</span></span>      | <span data-ttu-id="f67e7-213">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-213">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f67e7-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="f67e7-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f67e7-215">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="f67e7-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f67e7-216">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f67e7-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f67e7-217">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f67e7-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f67e7-218">Search-Flags</span></span>           | <span data-ttu-id="f67e7-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f67e7-219">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="f67e7-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f67e7-220">System-Flags</span></span>           | <span data-ttu-id="f67e7-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f67e7-221">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="f67e7-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f67e7-222">Classes used in</span></span>        | [<span data-ttu-id="f67e7-223">**Class-Store**</span><span class="sxs-lookup"><span data-stu-id="f67e7-223">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="f67e7-224">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="f67e7-224">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f67e7-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f67e7-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f67e7-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f67e7-226">Entry</span></span> | <span data-ttu-id="f67e7-227">Wert</span><span class="sxs-lookup"><span data-stu-id="f67e7-227">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f67e7-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f67e7-228">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f67e7-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f67e7-229">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f67e7-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="f67e7-230">System-Only</span></span>            | <span data-ttu-id="f67e7-231">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-231">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f67e7-232">Is-Single-Valued</span></span>       | <span data-ttu-id="f67e7-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="f67e7-233">True</span></span>                                                                                                            |
| <span data-ttu-id="f67e7-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f67e7-234">Is Indexed</span></span>             | <span data-ttu-id="f67e7-235">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-235">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f67e7-236">In Global Catalog</span></span>      | <span data-ttu-id="f67e7-237">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-237">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f67e7-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="f67e7-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f67e7-239">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="f67e7-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f67e7-240">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f67e7-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f67e7-241">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f67e7-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f67e7-242">Search-Flags</span></span>           | <span data-ttu-id="f67e7-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f67e7-243">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="f67e7-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f67e7-244">System-Flags</span></span>           | <span data-ttu-id="f67e7-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f67e7-245">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="f67e7-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f67e7-246">Classes used in</span></span>        | [<span data-ttu-id="f67e7-247">**Class-Store**</span><span class="sxs-lookup"><span data-stu-id="f67e7-247">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="f67e7-248">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="f67e7-248">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f67e7-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f67e7-249">Windows Server 2012</span></span>



| <span data-ttu-id="f67e7-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f67e7-250">Entry</span></span> | <span data-ttu-id="f67e7-251">Wert</span><span class="sxs-lookup"><span data-stu-id="f67e7-251">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f67e7-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f67e7-252">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f67e7-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f67e7-253">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="f67e7-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="f67e7-254">System-Only</span></span>            | <span data-ttu-id="f67e7-255">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-255">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f67e7-256">Is-Single-Valued</span></span>       | <span data-ttu-id="f67e7-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="f67e7-257">True</span></span>                                                                                                            |
| <span data-ttu-id="f67e7-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f67e7-258">Is Indexed</span></span>             | <span data-ttu-id="f67e7-259">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-259">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f67e7-260">In Global Catalog</span></span>      | <span data-ttu-id="f67e7-261">False</span><span class="sxs-lookup"><span data-stu-id="f67e7-261">False</span></span>                                                                                                           |
| <span data-ttu-id="f67e7-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f67e7-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="f67e7-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f67e7-263">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="f67e7-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f67e7-264">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f67e7-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f67e7-265">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="f67e7-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f67e7-266">Search-Flags</span></span>           | <span data-ttu-id="f67e7-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f67e7-267">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="f67e7-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f67e7-268">System-Flags</span></span>           | <span data-ttu-id="f67e7-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f67e7-269">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="f67e7-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f67e7-270">Classes used in</span></span>        | [<span data-ttu-id="f67e7-271">**Class-Store**</span><span class="sxs-lookup"><span data-stu-id="f67e7-271">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="f67e7-272">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="f67e7-272">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





