---
title: Rights-Guid-Attribut
description: Die GUID, die zum Darstellen eines erweiterten Rechts innerhalb eines Zugriffs Steuerungs Eintrags verwendet wird.
ms.assetid: 6f3a654e-fead-41e7-8383-6dade1a2747e
ms.tgt_platform: multiple
keywords:
- AD-Schema für Rights-Guid-Attribut
- rightsguid-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Rights-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da47ec8e4736dd13b6ba39da0208aed505aa8a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122690"
---
# <a name="rights-guid-attribute"></a><span data-ttu-id="f15b7-105">Rights-Guid-Attribut</span><span class="sxs-lookup"><span data-stu-id="f15b7-105">Rights-Guid attribute</span></span>

<span data-ttu-id="f15b7-106">Die GUID, die zum Darstellen eines erweiterten Rechts innerhalb eines Zugriffs Steuerungs Eintrags verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f15b7-106">The GUID used to represent an extended right within an access control entry.</span></span>



| <span data-ttu-id="f15b7-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f15b7-107">Entry</span></span> | <span data-ttu-id="f15b7-108">Wert</span><span class="sxs-lookup"><span data-stu-id="f15b7-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f15b7-109">CN</span><span class="sxs-lookup"><span data-stu-id="f15b7-109">CN</span></span>                | <span data-ttu-id="f15b7-110">Rights-Guid</span><span class="sxs-lookup"><span data-stu-id="f15b7-110">Rights-Guid</span></span>                                 |
| <span data-ttu-id="f15b7-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f15b7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f15b7-112">righguid</span><span class="sxs-lookup"><span data-stu-id="f15b7-112">rightsGuid</span></span>                                  |
| <span data-ttu-id="f15b7-113">Size</span><span class="sxs-lookup"><span data-stu-id="f15b7-113">Size</span></span>              | <span data-ttu-id="f15b7-114">16 Bytes</span><span class="sxs-lookup"><span data-stu-id="f15b7-114">16 bytes</span></span>                                    |
| <span data-ttu-id="f15b7-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f15b7-115">Update Privilege</span></span>  | <span data-ttu-id="f15b7-116">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f15b7-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="f15b7-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f15b7-117">Update Frequency</span></span>  | <span data-ttu-id="f15b7-118">Wenn ein neues erweitertes Recht erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f15b7-118">When a new extended right is created.</span></span>       |
| <span data-ttu-id="f15b7-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f15b7-119">Attribute-Id</span></span>      | <span data-ttu-id="f15b7-120">1.2.840.113556.1.4.340</span><span class="sxs-lookup"><span data-stu-id="f15b7-120">1.2.840.113556.1.4.340</span></span>                      |
| <span data-ttu-id="f15b7-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f15b7-121">System-Id-Guid</span></span>    | <span data-ttu-id="f15b7-122">8297931c-86d3-11D0-AFDA-00c04f 930c9</span><span class="sxs-lookup"><span data-stu-id="f15b7-122">8297931c-86d3-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="f15b7-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="f15b7-123">Syntax</span></span>            | [<span data-ttu-id="f15b7-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f15b7-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f15b7-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f15b7-125">Implementations</span></span>

-   [<span data-ttu-id="f15b7-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f15b7-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f15b7-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f15b7-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f15b7-128">**Adam**</span><span class="sxs-lookup"><span data-stu-id="f15b7-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f15b7-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f15b7-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f15b7-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f15b7-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f15b7-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f15b7-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f15b7-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f15b7-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f15b7-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f15b7-133">Windows 2000 Server</span></span>



| <span data-ttu-id="f15b7-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f15b7-134">Entry</span></span> | <span data-ttu-id="f15b7-135">Wert</span><span class="sxs-lookup"><span data-stu-id="f15b7-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="f15b7-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f15b7-136">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="f15b7-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f15b7-137">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="f15b7-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="f15b7-138">System-Only</span></span>            | <span data-ttu-id="f15b7-139">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-139">False</span></span>                                                           |
| <span data-ttu-id="f15b7-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f15b7-140">Is-Single-Valued</span></span>       | <span data-ttu-id="f15b7-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="f15b7-141">True</span></span>                                                            |
| <span data-ttu-id="f15b7-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f15b7-142">Is Indexed</span></span>             | <span data-ttu-id="f15b7-143">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-143">False</span></span>                                                           |
| <span data-ttu-id="f15b7-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f15b7-144">In Global Catalog</span></span>      | <span data-ttu-id="f15b7-145">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-145">False</span></span>                                                           |
| <span data-ttu-id="f15b7-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f15b7-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="f15b7-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f15b7-147">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="f15b7-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f15b7-148">Range-Lower</span></span>            | <span data-ttu-id="f15b7-149">36</span><span class="sxs-lookup"><span data-stu-id="f15b7-149">36</span></span>                                                              |
| <span data-ttu-id="f15b7-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f15b7-150">Range-Upper</span></span>            | <span data-ttu-id="f15b7-151">36</span><span class="sxs-lookup"><span data-stu-id="f15b7-151">36</span></span>                                                              |
| <span data-ttu-id="f15b7-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f15b7-152">Search-Flags</span></span>           | <span data-ttu-id="f15b7-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f15b7-153">0x00000000</span></span>                                                      |
| <span data-ttu-id="f15b7-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f15b7-154">System-Flags</span></span>           | <span data-ttu-id="f15b7-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f15b7-155">0x00000010</span></span>                                                      |
| <span data-ttu-id="f15b7-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f15b7-156">Classes used in</span></span>        | [<span data-ttu-id="f15b7-157">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="f15b7-157">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f15b7-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f15b7-158">Windows Server 2003</span></span>



| <span data-ttu-id="f15b7-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f15b7-159">Entry</span></span> | <span data-ttu-id="f15b7-160">Wert</span><span class="sxs-lookup"><span data-stu-id="f15b7-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="f15b7-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f15b7-161">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="f15b7-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f15b7-162">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="f15b7-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="f15b7-163">System-Only</span></span>            | <span data-ttu-id="f15b7-164">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-164">False</span></span>                                                           |
| <span data-ttu-id="f15b7-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f15b7-165">Is-Single-Valued</span></span>       | <span data-ttu-id="f15b7-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="f15b7-166">True</span></span>                                                            |
| <span data-ttu-id="f15b7-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f15b7-167">Is Indexed</span></span>             | <span data-ttu-id="f15b7-168">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-168">False</span></span>                                                           |
| <span data-ttu-id="f15b7-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f15b7-169">In Global Catalog</span></span>      | <span data-ttu-id="f15b7-170">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-170">False</span></span>                                                           |
| <span data-ttu-id="f15b7-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f15b7-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="f15b7-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f15b7-172">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="f15b7-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f15b7-173">Range-Lower</span></span>            | <span data-ttu-id="f15b7-174">36</span><span class="sxs-lookup"><span data-stu-id="f15b7-174">36</span></span>                                                              |
| <span data-ttu-id="f15b7-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f15b7-175">Range-Upper</span></span>            | <span data-ttu-id="f15b7-176">36</span><span class="sxs-lookup"><span data-stu-id="f15b7-176">36</span></span>                                                              |
| <span data-ttu-id="f15b7-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f15b7-177">Search-Flags</span></span>           | <span data-ttu-id="f15b7-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f15b7-178">0x00000000</span></span>                                                      |
| <span data-ttu-id="f15b7-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f15b7-179">System-Flags</span></span>           | <span data-ttu-id="f15b7-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f15b7-180">0x00000010</span></span>                                                      |
| <span data-ttu-id="f15b7-181">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f15b7-181">Classes used in</span></span>        | [<span data-ttu-id="f15b7-182">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="f15b7-182">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f15b7-183">Adam</span><span class="sxs-lookup"><span data-stu-id="f15b7-183">ADAM</span></span>



| <span data-ttu-id="f15b7-184">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f15b7-184">Entry</span></span> | <span data-ttu-id="f15b7-185">Wert</span><span class="sxs-lookup"><span data-stu-id="f15b7-185">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="f15b7-186">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f15b7-186">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="f15b7-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f15b7-187">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="f15b7-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="f15b7-188">System-Only</span></span>            | <span data-ttu-id="f15b7-189">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-189">False</span></span>                                                           |
| <span data-ttu-id="f15b7-190">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f15b7-190">Is-Single-Valued</span></span>       | <span data-ttu-id="f15b7-191">Richtig</span><span class="sxs-lookup"><span data-stu-id="f15b7-191">True</span></span>                                                            |
| <span data-ttu-id="f15b7-192">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f15b7-192">Is Indexed</span></span>             | <span data-ttu-id="f15b7-193">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-193">False</span></span>                                                           |
| <span data-ttu-id="f15b7-194">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f15b7-194">In Global Catalog</span></span>      | <span data-ttu-id="f15b7-195">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-195">False</span></span>                                                           |
| <span data-ttu-id="f15b7-196">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f15b7-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="f15b7-197">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f15b7-197">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="f15b7-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f15b7-198">Range-Lower</span></span>            | <span data-ttu-id="f15b7-199">36</span><span class="sxs-lookup"><span data-stu-id="f15b7-199">36</span></span>                                                              |
| <span data-ttu-id="f15b7-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f15b7-200">Range-Upper</span></span>            | <span data-ttu-id="f15b7-201">36</span><span class="sxs-lookup"><span data-stu-id="f15b7-201">36</span></span>                                                              |
| <span data-ttu-id="f15b7-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f15b7-202">Search-Flags</span></span>           | <span data-ttu-id="f15b7-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f15b7-203">0x00000000</span></span>                                                      |
| <span data-ttu-id="f15b7-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f15b7-204">System-Flags</span></span>           | <span data-ttu-id="f15b7-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f15b7-205">0x00000010</span></span>                                                      |
| <span data-ttu-id="f15b7-206">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f15b7-206">Classes used in</span></span>        | [<span data-ttu-id="f15b7-207">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="f15b7-207">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f15b7-208">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f15b7-208">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f15b7-209">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f15b7-209">Entry</span></span> | <span data-ttu-id="f15b7-210">Wert</span><span class="sxs-lookup"><span data-stu-id="f15b7-210">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="f15b7-211">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f15b7-211">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="f15b7-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f15b7-212">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="f15b7-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="f15b7-213">System-Only</span></span>            | <span data-ttu-id="f15b7-214">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-214">False</span></span>                                                           |
| <span data-ttu-id="f15b7-215">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f15b7-215">Is-Single-Valued</span></span>       | <span data-ttu-id="f15b7-216">Richtig</span><span class="sxs-lookup"><span data-stu-id="f15b7-216">True</span></span>                                                            |
| <span data-ttu-id="f15b7-217">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f15b7-217">Is Indexed</span></span>             | <span data-ttu-id="f15b7-218">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-218">False</span></span>                                                           |
| <span data-ttu-id="f15b7-219">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f15b7-219">In Global Catalog</span></span>      | <span data-ttu-id="f15b7-220">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-220">False</span></span>                                                           |
| <span data-ttu-id="f15b7-221">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f15b7-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="f15b7-222">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f15b7-222">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="f15b7-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f15b7-223">Range-Lower</span></span>            | <span data-ttu-id="f15b7-224">36</span><span class="sxs-lookup"><span data-stu-id="f15b7-224">36</span></span>                                                              |
| <span data-ttu-id="f15b7-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f15b7-225">Range-Upper</span></span>            | <span data-ttu-id="f15b7-226">36</span><span class="sxs-lookup"><span data-stu-id="f15b7-226">36</span></span>                                                              |
| <span data-ttu-id="f15b7-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f15b7-227">Search-Flags</span></span>           | <span data-ttu-id="f15b7-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f15b7-228">0x00000000</span></span>                                                      |
| <span data-ttu-id="f15b7-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f15b7-229">System-Flags</span></span>           | <span data-ttu-id="f15b7-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f15b7-230">0x00000010</span></span>                                                      |
| <span data-ttu-id="f15b7-231">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f15b7-231">Classes used in</span></span>        | [<span data-ttu-id="f15b7-232">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="f15b7-232">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f15b7-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f15b7-233">Windows Server 2008</span></span>



| <span data-ttu-id="f15b7-234">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f15b7-234">Entry</span></span> | <span data-ttu-id="f15b7-235">Wert</span><span class="sxs-lookup"><span data-stu-id="f15b7-235">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="f15b7-236">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f15b7-236">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="f15b7-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f15b7-237">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="f15b7-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="f15b7-238">System-Only</span></span>            | <span data-ttu-id="f15b7-239">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-239">False</span></span>                                                           |
| <span data-ttu-id="f15b7-240">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f15b7-240">Is-Single-Valued</span></span>       | <span data-ttu-id="f15b7-241">Richtig</span><span class="sxs-lookup"><span data-stu-id="f15b7-241">True</span></span>                                                            |
| <span data-ttu-id="f15b7-242">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f15b7-242">Is Indexed</span></span>             | <span data-ttu-id="f15b7-243">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-243">False</span></span>                                                           |
| <span data-ttu-id="f15b7-244">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f15b7-244">In Global Catalog</span></span>      | <span data-ttu-id="f15b7-245">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-245">False</span></span>                                                           |
| <span data-ttu-id="f15b7-246">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f15b7-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="f15b7-247">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f15b7-247">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="f15b7-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f15b7-248">Range-Lower</span></span>            | <span data-ttu-id="f15b7-249">36</span><span class="sxs-lookup"><span data-stu-id="f15b7-249">36</span></span>                                                              |
| <span data-ttu-id="f15b7-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f15b7-250">Range-Upper</span></span>            | <span data-ttu-id="f15b7-251">36</span><span class="sxs-lookup"><span data-stu-id="f15b7-251">36</span></span>                                                              |
| <span data-ttu-id="f15b7-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f15b7-252">Search-Flags</span></span>           | <span data-ttu-id="f15b7-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f15b7-253">0x00000000</span></span>                                                      |
| <span data-ttu-id="f15b7-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f15b7-254">System-Flags</span></span>           | <span data-ttu-id="f15b7-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f15b7-255">0x00000010</span></span>                                                      |
| <span data-ttu-id="f15b7-256">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f15b7-256">Classes used in</span></span>        | [<span data-ttu-id="f15b7-257">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="f15b7-257">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f15b7-258">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f15b7-258">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f15b7-259">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f15b7-259">Entry</span></span> | <span data-ttu-id="f15b7-260">Wert</span><span class="sxs-lookup"><span data-stu-id="f15b7-260">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="f15b7-261">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f15b7-261">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="f15b7-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f15b7-262">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="f15b7-263">System-Only</span><span class="sxs-lookup"><span data-stu-id="f15b7-263">System-Only</span></span>            | <span data-ttu-id="f15b7-264">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-264">False</span></span>                                                           |
| <span data-ttu-id="f15b7-265">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f15b7-265">Is-Single-Valued</span></span>       | <span data-ttu-id="f15b7-266">Richtig</span><span class="sxs-lookup"><span data-stu-id="f15b7-266">True</span></span>                                                            |
| <span data-ttu-id="f15b7-267">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f15b7-267">Is Indexed</span></span>             | <span data-ttu-id="f15b7-268">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-268">False</span></span>                                                           |
| <span data-ttu-id="f15b7-269">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f15b7-269">In Global Catalog</span></span>      | <span data-ttu-id="f15b7-270">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-270">False</span></span>                                                           |
| <span data-ttu-id="f15b7-271">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f15b7-271">NT-Security-Descriptor</span></span> | <span data-ttu-id="f15b7-272">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f15b7-272">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="f15b7-273">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f15b7-273">Range-Lower</span></span>            | <span data-ttu-id="f15b7-274">36</span><span class="sxs-lookup"><span data-stu-id="f15b7-274">36</span></span>                                                              |
| <span data-ttu-id="f15b7-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f15b7-275">Range-Upper</span></span>            | <span data-ttu-id="f15b7-276">36</span><span class="sxs-lookup"><span data-stu-id="f15b7-276">36</span></span>                                                              |
| <span data-ttu-id="f15b7-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f15b7-277">Search-Flags</span></span>           | <span data-ttu-id="f15b7-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f15b7-278">0x00000000</span></span>                                                      |
| <span data-ttu-id="f15b7-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f15b7-279">System-Flags</span></span>           | <span data-ttu-id="f15b7-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f15b7-280">0x00000010</span></span>                                                      |
| <span data-ttu-id="f15b7-281">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f15b7-281">Classes used in</span></span>        | [<span data-ttu-id="f15b7-282">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="f15b7-282">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f15b7-283">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f15b7-283">Windows Server 2012</span></span>



| <span data-ttu-id="f15b7-284">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f15b7-284">Entry</span></span> | <span data-ttu-id="f15b7-285">Wert</span><span class="sxs-lookup"><span data-stu-id="f15b7-285">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="f15b7-286">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f15b7-286">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="f15b7-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f15b7-287">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="f15b7-288">System-Only</span><span class="sxs-lookup"><span data-stu-id="f15b7-288">System-Only</span></span>            | <span data-ttu-id="f15b7-289">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-289">False</span></span>                                                           |
| <span data-ttu-id="f15b7-290">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f15b7-290">Is-Single-Valued</span></span>       | <span data-ttu-id="f15b7-291">Richtig</span><span class="sxs-lookup"><span data-stu-id="f15b7-291">True</span></span>                                                            |
| <span data-ttu-id="f15b7-292">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f15b7-292">Is Indexed</span></span>             | <span data-ttu-id="f15b7-293">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-293">False</span></span>                                                           |
| <span data-ttu-id="f15b7-294">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f15b7-294">In Global Catalog</span></span>      | <span data-ttu-id="f15b7-295">False</span><span class="sxs-lookup"><span data-stu-id="f15b7-295">False</span></span>                                                           |
| <span data-ttu-id="f15b7-296">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f15b7-296">NT-Security-Descriptor</span></span> | <span data-ttu-id="f15b7-297">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f15b7-297">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="f15b7-298">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f15b7-298">Range-Lower</span></span>            | <span data-ttu-id="f15b7-299">36</span><span class="sxs-lookup"><span data-stu-id="f15b7-299">36</span></span>                                                              |
| <span data-ttu-id="f15b7-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f15b7-300">Range-Upper</span></span>            | <span data-ttu-id="f15b7-301">36</span><span class="sxs-lookup"><span data-stu-id="f15b7-301">36</span></span>                                                              |
| <span data-ttu-id="f15b7-302">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f15b7-302">Search-Flags</span></span>           | <span data-ttu-id="f15b7-303">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f15b7-303">0x00000000</span></span>                                                      |
| <span data-ttu-id="f15b7-304">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f15b7-304">System-Flags</span></span>           | <span data-ttu-id="f15b7-305">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f15b7-305">0x00000010</span></span>                                                      |
| <span data-ttu-id="f15b7-306">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f15b7-306">Classes used in</span></span>        | [<span data-ttu-id="f15b7-307">**Control-Access-Right**</span><span class="sxs-lookup"><span data-stu-id="f15b7-307">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





