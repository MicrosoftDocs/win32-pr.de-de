---
title: Transport-DLL-Name-Attribut
description: Der Name der dll, von der ein Transport verwaltet wird.
ms.assetid: a6b078ec-8738-4c57-9d94-05a96dbc645b
ms.tgt_platform: multiple
keywords:
- AD-Schema für Transport-DLL-Name-Attribut
- transportdllname-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Transport-DLL-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c118a2f7553c86de4b3c36b2904a3b7d75518a2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346569"
---
# <a name="transport-dll-name-attribute"></a><span data-ttu-id="9a4d5-105">Transport-DLL-Name-Attribut</span><span class="sxs-lookup"><span data-stu-id="9a4d5-105">Transport-DLL-Name attribute</span></span>

<span data-ttu-id="9a4d5-106">Der Name der dll, von der ein Transport verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="9a4d5-106">The name of the DLL that will manage a transport.</span></span>



| <span data-ttu-id="9a4d5-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a4d5-107">Entry</span></span> | <span data-ttu-id="9a4d5-108">Wert</span><span class="sxs-lookup"><span data-stu-id="9a4d5-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9a4d5-109">CN</span><span class="sxs-lookup"><span data-stu-id="9a4d5-109">CN</span></span>                | <span data-ttu-id="9a4d5-110">Transport-DLL-Name</span><span class="sxs-lookup"><span data-stu-id="9a4d5-110">Transport-DLL-Name</span></span>                          |
| <span data-ttu-id="9a4d5-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9a4d5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9a4d5-112">transportdllname</span><span class="sxs-lookup"><span data-stu-id="9a4d5-112">transportDLLName</span></span>                            |
| <span data-ttu-id="9a4d5-113">Size</span><span class="sxs-lookup"><span data-stu-id="9a4d5-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="9a4d5-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="9a4d5-114">Update Privilege</span></span>  | <span data-ttu-id="9a4d5-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9a4d5-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="9a4d5-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="9a4d5-116">Update Frequency</span></span>  | <span data-ttu-id="9a4d5-117">Beim Verbinden von Standorten.</span><span class="sxs-lookup"><span data-stu-id="9a4d5-117">When connecting sites.</span></span>                      |
| <span data-ttu-id="9a4d5-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9a4d5-118">Attribute-Id</span></span>      | <span data-ttu-id="9a4d5-119">1.2.840.113556.1.4.789</span><span class="sxs-lookup"><span data-stu-id="9a4d5-119">1.2.840.113556.1.4.789</span></span>                      |
| <span data-ttu-id="9a4d5-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9a4d5-120">System-Id-Guid</span></span>    | <span data-ttu-id="9a4d5-121">26d97372-6070-11d1-a9c6-0000b80367c1</span><span class="sxs-lookup"><span data-stu-id="9a4d5-121">26d97372-6070-11d1-a9c6-0000f80367c1</span></span>        |
| <span data-ttu-id="9a4d5-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a4d5-122">Syntax</span></span>            | [<span data-ttu-id="9a4d5-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9a4d5-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9a4d5-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="9a4d5-124">Implementations</span></span>

-   [<span data-ttu-id="9a4d5-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9a4d5-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9a4d5-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9a4d5-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9a4d5-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="9a4d5-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9a4d5-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9a4d5-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9a4d5-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9a4d5-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9a4d5-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9a4d5-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9a4d5-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9a4d5-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9a4d5-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9a4d5-132">Windows 2000 Server</span></span>



| <span data-ttu-id="9a4d5-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a4d5-133">Entry</span></span> | <span data-ttu-id="9a4d5-134">Wert</span><span class="sxs-lookup"><span data-stu-id="9a4d5-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9a4d5-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a4d5-135">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9a4d5-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a4d5-136">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9a4d5-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a4d5-137">System-Only</span></span>            | <span data-ttu-id="9a4d5-138">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-138">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a4d5-139">Is-Single-Valued</span></span>       | <span data-ttu-id="9a4d5-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a4d5-140">True</span></span>                                                            |
| <span data-ttu-id="9a4d5-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a4d5-141">Is Indexed</span></span>             | <span data-ttu-id="9a4d5-142">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-142">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a4d5-143">In Global Catalog</span></span>      | <span data-ttu-id="9a4d5-144">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-144">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a4d5-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a4d5-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a4d5-146">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9a4d5-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a4d5-147">Range-Lower</span></span>            | <span data-ttu-id="9a4d5-148">0</span><span class="sxs-lookup"><span data-stu-id="9a4d5-148">0</span></span>                                                               |
| <span data-ttu-id="9a4d5-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a4d5-149">Range-Upper</span></span>            | <span data-ttu-id="9a4d5-150">1024</span><span class="sxs-lookup"><span data-stu-id="9a4d5-150">1024</span></span>                                                            |
| <span data-ttu-id="9a4d5-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a4d5-151">Search-Flags</span></span>           | <span data-ttu-id="9a4d5-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a4d5-152">0x00000000</span></span>                                                      |
| <span data-ttu-id="9a4d5-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a4d5-153">System-Flags</span></span>           | <span data-ttu-id="9a4d5-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a4d5-154">0x00000010</span></span>                                                      |
| <span data-ttu-id="9a4d5-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a4d5-155">Classes used in</span></span>        | [<span data-ttu-id="9a4d5-156">**Standort übergreifender Transport**</span><span class="sxs-lookup"><span data-stu-id="9a4d5-156">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9a4d5-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9a4d5-157">Windows Server 2003</span></span>



| <span data-ttu-id="9a4d5-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a4d5-158">Entry</span></span> | <span data-ttu-id="9a4d5-159">Wert</span><span class="sxs-lookup"><span data-stu-id="9a4d5-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9a4d5-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a4d5-160">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9a4d5-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a4d5-161">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9a4d5-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a4d5-162">System-Only</span></span>            | <span data-ttu-id="9a4d5-163">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-163">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a4d5-164">Is-Single-Valued</span></span>       | <span data-ttu-id="9a4d5-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a4d5-165">True</span></span>                                                            |
| <span data-ttu-id="9a4d5-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a4d5-166">Is Indexed</span></span>             | <span data-ttu-id="9a4d5-167">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-167">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a4d5-168">In Global Catalog</span></span>      | <span data-ttu-id="9a4d5-169">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-169">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a4d5-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a4d5-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a4d5-171">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9a4d5-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a4d5-172">Range-Lower</span></span>            | <span data-ttu-id="9a4d5-173">0</span><span class="sxs-lookup"><span data-stu-id="9a4d5-173">0</span></span>                                                               |
| <span data-ttu-id="9a4d5-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a4d5-174">Range-Upper</span></span>            | <span data-ttu-id="9a4d5-175">1024</span><span class="sxs-lookup"><span data-stu-id="9a4d5-175">1024</span></span>                                                            |
| <span data-ttu-id="9a4d5-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a4d5-176">Search-Flags</span></span>           | <span data-ttu-id="9a4d5-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a4d5-177">0x00000000</span></span>                                                      |
| <span data-ttu-id="9a4d5-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a4d5-178">System-Flags</span></span>           | <span data-ttu-id="9a4d5-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a4d5-179">0x00000010</span></span>                                                      |
| <span data-ttu-id="9a4d5-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a4d5-180">Classes used in</span></span>        | [<span data-ttu-id="9a4d5-181">**Standort übergreifender Transport**</span><span class="sxs-lookup"><span data-stu-id="9a4d5-181">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9a4d5-182">Adam</span><span class="sxs-lookup"><span data-stu-id="9a4d5-182">ADAM</span></span>



| <span data-ttu-id="9a4d5-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a4d5-183">Entry</span></span> | <span data-ttu-id="9a4d5-184">Wert</span><span class="sxs-lookup"><span data-stu-id="9a4d5-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9a4d5-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a4d5-185">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9a4d5-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a4d5-186">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9a4d5-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a4d5-187">System-Only</span></span>            | <span data-ttu-id="9a4d5-188">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-188">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a4d5-189">Is-Single-Valued</span></span>       | <span data-ttu-id="9a4d5-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a4d5-190">True</span></span>                                                            |
| <span data-ttu-id="9a4d5-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a4d5-191">Is Indexed</span></span>             | <span data-ttu-id="9a4d5-192">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-192">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a4d5-193">In Global Catalog</span></span>      | <span data-ttu-id="9a4d5-194">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-194">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a4d5-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a4d5-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a4d5-196">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9a4d5-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a4d5-197">Range-Lower</span></span>            | <span data-ttu-id="9a4d5-198">0</span><span class="sxs-lookup"><span data-stu-id="9a4d5-198">0</span></span>                                                               |
| <span data-ttu-id="9a4d5-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a4d5-199">Range-Upper</span></span>            | <span data-ttu-id="9a4d5-200">1024</span><span class="sxs-lookup"><span data-stu-id="9a4d5-200">1024</span></span>                                                            |
| <span data-ttu-id="9a4d5-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a4d5-201">Search-Flags</span></span>           | <span data-ttu-id="9a4d5-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a4d5-202">0x00000000</span></span>                                                      |
| <span data-ttu-id="9a4d5-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a4d5-203">System-Flags</span></span>           | <span data-ttu-id="9a4d5-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a4d5-204">0x00000010</span></span>                                                      |
| <span data-ttu-id="9a4d5-205">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a4d5-205">Classes used in</span></span>        | [<span data-ttu-id="9a4d5-206">**Standort übergreifender Transport**</span><span class="sxs-lookup"><span data-stu-id="9a4d5-206">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9a4d5-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9a4d5-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9a4d5-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a4d5-208">Entry</span></span> | <span data-ttu-id="9a4d5-209">Wert</span><span class="sxs-lookup"><span data-stu-id="9a4d5-209">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9a4d5-210">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a4d5-210">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9a4d5-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a4d5-211">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9a4d5-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a4d5-212">System-Only</span></span>            | <span data-ttu-id="9a4d5-213">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-213">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-214">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a4d5-214">Is-Single-Valued</span></span>       | <span data-ttu-id="9a4d5-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a4d5-215">True</span></span>                                                            |
| <span data-ttu-id="9a4d5-216">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a4d5-216">Is Indexed</span></span>             | <span data-ttu-id="9a4d5-217">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-217">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-218">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a4d5-218">In Global Catalog</span></span>      | <span data-ttu-id="9a4d5-219">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-219">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a4d5-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a4d5-221">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a4d5-221">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9a4d5-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a4d5-222">Range-Lower</span></span>            | <span data-ttu-id="9a4d5-223">0</span><span class="sxs-lookup"><span data-stu-id="9a4d5-223">0</span></span>                                                               |
| <span data-ttu-id="9a4d5-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a4d5-224">Range-Upper</span></span>            | <span data-ttu-id="9a4d5-225">1024</span><span class="sxs-lookup"><span data-stu-id="9a4d5-225">1024</span></span>                                                            |
| <span data-ttu-id="9a4d5-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a4d5-226">Search-Flags</span></span>           | <span data-ttu-id="9a4d5-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a4d5-227">0x00000000</span></span>                                                      |
| <span data-ttu-id="9a4d5-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a4d5-228">System-Flags</span></span>           | <span data-ttu-id="9a4d5-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a4d5-229">0x00000010</span></span>                                                      |
| <span data-ttu-id="9a4d5-230">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a4d5-230">Classes used in</span></span>        | [<span data-ttu-id="9a4d5-231">**Standort übergreifender Transport**</span><span class="sxs-lookup"><span data-stu-id="9a4d5-231">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9a4d5-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a4d5-232">Windows Server 2008</span></span>



| <span data-ttu-id="9a4d5-233">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a4d5-233">Entry</span></span> | <span data-ttu-id="9a4d5-234">Wert</span><span class="sxs-lookup"><span data-stu-id="9a4d5-234">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9a4d5-235">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a4d5-235">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9a4d5-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a4d5-236">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9a4d5-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a4d5-237">System-Only</span></span>            | <span data-ttu-id="9a4d5-238">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-238">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-239">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a4d5-239">Is-Single-Valued</span></span>       | <span data-ttu-id="9a4d5-240">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a4d5-240">True</span></span>                                                            |
| <span data-ttu-id="9a4d5-241">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a4d5-241">Is Indexed</span></span>             | <span data-ttu-id="9a4d5-242">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-242">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-243">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a4d5-243">In Global Catalog</span></span>      | <span data-ttu-id="9a4d5-244">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-244">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a4d5-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a4d5-246">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a4d5-246">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9a4d5-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a4d5-247">Range-Lower</span></span>            | <span data-ttu-id="9a4d5-248">0</span><span class="sxs-lookup"><span data-stu-id="9a4d5-248">0</span></span>                                                               |
| <span data-ttu-id="9a4d5-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a4d5-249">Range-Upper</span></span>            | <span data-ttu-id="9a4d5-250">1024</span><span class="sxs-lookup"><span data-stu-id="9a4d5-250">1024</span></span>                                                            |
| <span data-ttu-id="9a4d5-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a4d5-251">Search-Flags</span></span>           | <span data-ttu-id="9a4d5-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a4d5-252">0x00000000</span></span>                                                      |
| <span data-ttu-id="9a4d5-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a4d5-253">System-Flags</span></span>           | <span data-ttu-id="9a4d5-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a4d5-254">0x00000010</span></span>                                                      |
| <span data-ttu-id="9a4d5-255">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a4d5-255">Classes used in</span></span>        | [<span data-ttu-id="9a4d5-256">**Standort übergreifender Transport**</span><span class="sxs-lookup"><span data-stu-id="9a4d5-256">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9a4d5-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9a4d5-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9a4d5-258">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a4d5-258">Entry</span></span> | <span data-ttu-id="9a4d5-259">Wert</span><span class="sxs-lookup"><span data-stu-id="9a4d5-259">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9a4d5-260">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a4d5-260">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9a4d5-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a4d5-261">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9a4d5-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a4d5-262">System-Only</span></span>            | <span data-ttu-id="9a4d5-263">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-263">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-264">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a4d5-264">Is-Single-Valued</span></span>       | <span data-ttu-id="9a4d5-265">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a4d5-265">True</span></span>                                                            |
| <span data-ttu-id="9a4d5-266">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a4d5-266">Is Indexed</span></span>             | <span data-ttu-id="9a4d5-267">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-267">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-268">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a4d5-268">In Global Catalog</span></span>      | <span data-ttu-id="9a4d5-269">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-269">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-270">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a4d5-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a4d5-271">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a4d5-271">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9a4d5-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a4d5-272">Range-Lower</span></span>            | <span data-ttu-id="9a4d5-273">0</span><span class="sxs-lookup"><span data-stu-id="9a4d5-273">0</span></span>                                                               |
| <span data-ttu-id="9a4d5-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a4d5-274">Range-Upper</span></span>            | <span data-ttu-id="9a4d5-275">1024</span><span class="sxs-lookup"><span data-stu-id="9a4d5-275">1024</span></span>                                                            |
| <span data-ttu-id="9a4d5-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a4d5-276">Search-Flags</span></span>           | <span data-ttu-id="9a4d5-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a4d5-277">0x00000000</span></span>                                                      |
| <span data-ttu-id="9a4d5-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a4d5-278">System-Flags</span></span>           | <span data-ttu-id="9a4d5-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a4d5-279">0x00000010</span></span>                                                      |
| <span data-ttu-id="9a4d5-280">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a4d5-280">Classes used in</span></span>        | [<span data-ttu-id="9a4d5-281">**Standort übergreifender Transport**</span><span class="sxs-lookup"><span data-stu-id="9a4d5-281">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9a4d5-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9a4d5-282">Windows Server 2012</span></span>



| <span data-ttu-id="9a4d5-283">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a4d5-283">Entry</span></span> | <span data-ttu-id="9a4d5-284">Wert</span><span class="sxs-lookup"><span data-stu-id="9a4d5-284">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9a4d5-285">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a4d5-285">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9a4d5-286">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a4d5-286">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="9a4d5-287">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a4d5-287">System-Only</span></span>            | <span data-ttu-id="9a4d5-288">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-288">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-289">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a4d5-289">Is-Single-Valued</span></span>       | <span data-ttu-id="9a4d5-290">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a4d5-290">True</span></span>                                                            |
| <span data-ttu-id="9a4d5-291">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a4d5-291">Is Indexed</span></span>             | <span data-ttu-id="9a4d5-292">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-292">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-293">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a4d5-293">In Global Catalog</span></span>      | <span data-ttu-id="9a4d5-294">False</span><span class="sxs-lookup"><span data-stu-id="9a4d5-294">False</span></span>                                                           |
| <span data-ttu-id="9a4d5-295">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a4d5-295">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a4d5-296">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a4d5-296">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="9a4d5-297">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a4d5-297">Range-Lower</span></span>            | <span data-ttu-id="9a4d5-298">0</span><span class="sxs-lookup"><span data-stu-id="9a4d5-298">0</span></span>                                                               |
| <span data-ttu-id="9a4d5-299">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a4d5-299">Range-Upper</span></span>            | <span data-ttu-id="9a4d5-300">1024</span><span class="sxs-lookup"><span data-stu-id="9a4d5-300">1024</span></span>                                                            |
| <span data-ttu-id="9a4d5-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a4d5-301">Search-Flags</span></span>           | <span data-ttu-id="9a4d5-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a4d5-302">0x00000000</span></span>                                                      |
| <span data-ttu-id="9a4d5-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a4d5-303">System-Flags</span></span>           | <span data-ttu-id="9a4d5-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9a4d5-304">0x00000010</span></span>                                                      |
| <span data-ttu-id="9a4d5-305">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a4d5-305">Classes used in</span></span>        | [<span data-ttu-id="9a4d5-306">**Standort übergreifender Transport**</span><span class="sxs-lookup"><span data-stu-id="9a4d5-306">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



 

 





