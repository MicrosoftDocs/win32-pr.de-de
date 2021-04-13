---
title: MS-TAPI-Unique-Identifier-Attribut
description: Stellt den Namen einer TAPI-Multicast Konferenz bereit. Dabei handelt es sich um das Naming-Attribut der Rt-Conference-Klasse.
ms.assetid: a8162af7-0169-4381-8edc-3dbbf178e8ed
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-TAPI-Unique-Identifier-Attribut
- AD-Schema des MSTAPI-UID-Attributs
topic_type:
- apiref
api_name:
- ms-TAPI-Unique-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 528d34d9d4282dac3f5bd5a41231094fd2666c2c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392274"
---
# <a name="ms-tapi-unique-identifier-attribute"></a><span data-ttu-id="f21ca-106">MS-TAPI-Unique-Identifier-Attribut</span><span class="sxs-lookup"><span data-stu-id="f21ca-106">ms-TAPI-Unique-Identifier attribute</span></span>

<span data-ttu-id="f21ca-107">Stellt den Namen einer TAPI-Multicast Konferenz bereit.</span><span class="sxs-lookup"><span data-stu-id="f21ca-107">Provides the name of a TAPI multicast conference.</span></span> <span data-ttu-id="f21ca-108">Dabei handelt es sich um das Naming-Attribut der Rt-Conference-Klasse.</span><span class="sxs-lookup"><span data-stu-id="f21ca-108">It is the naming attribute of the Rt-Conference class.</span></span>



| <span data-ttu-id="f21ca-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f21ca-109">Entry</span></span> | <span data-ttu-id="f21ca-110">Wert</span><span class="sxs-lookup"><span data-stu-id="f21ca-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="f21ca-111">CN</span><span class="sxs-lookup"><span data-stu-id="f21ca-111">CN</span></span>                | <span data-ttu-id="f21ca-112">MS-TAPI-Unique-Identifier</span><span class="sxs-lookup"><span data-stu-id="f21ca-112">ms-TAPI-Unique-Identifier</span></span>                                             |
| <span data-ttu-id="f21ca-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f21ca-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f21ca-114">MSTAPI-UID</span><span class="sxs-lookup"><span data-stu-id="f21ca-114">msTAPI-uid</span></span>                                                            |
| <span data-ttu-id="f21ca-115">Size</span><span class="sxs-lookup"><span data-stu-id="f21ca-115">Size</span></span>              | <span data-ttu-id="f21ca-116">Kann eine beliebige Zeichenfolge sein, in der Regel mit einer Länge von 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f21ca-116">Can be an arbitrary string, typically under 100 characters in length.</span></span> |
| <span data-ttu-id="f21ca-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f21ca-117">Update Privilege</span></span>  | <span data-ttu-id="f21ca-118">Es sind keine besonderen Berechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f21ca-118">No special privileges required.</span></span>                                       |
| <span data-ttu-id="f21ca-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f21ca-119">Update Frequency</span></span>  | <span data-ttu-id="f21ca-120">Wird einmal zum Zeitpunkt der Erstellung des Rt-Conference Objekts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f21ca-120">Set once at the time of creating the Rt-Conference object.</span></span>            |
| <span data-ttu-id="f21ca-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f21ca-121">Attribute-Id</span></span>      | <span data-ttu-id="f21ca-122">1.2.840.113556.1.4.1698</span><span class="sxs-lookup"><span data-stu-id="f21ca-122">1.2.840.113556.1.4.1698</span></span>                                               |
| <span data-ttu-id="f21ca-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f21ca-123">System-Id-Guid</span></span>    | <span data-ttu-id="f21ca-124">70a4e7ea-b3b9-4643-8918-e6dd2471bbd4</span><span class="sxs-lookup"><span data-stu-id="f21ca-124">70a4e7ea-b3b9-4643-8918-e6dd2471bfd4</span></span>                                  |
| <span data-ttu-id="f21ca-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="f21ca-125">Syntax</span></span>            | [<span data-ttu-id="f21ca-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f21ca-126">**String(Unicode)**</span></span>](s-string-unicode.md)                           |



## <a name="implementations"></a><span data-ttu-id="f21ca-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f21ca-127">Implementations</span></span>

-   [<span data-ttu-id="f21ca-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f21ca-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f21ca-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f21ca-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f21ca-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f21ca-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f21ca-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f21ca-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f21ca-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f21ca-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f21ca-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f21ca-133">Windows Server 2003</span></span>



| <span data-ttu-id="f21ca-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f21ca-134">Entry</span></span> | <span data-ttu-id="f21ca-135">Wert</span><span class="sxs-lookup"><span data-stu-id="f21ca-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f21ca-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f21ca-136">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="f21ca-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f21ca-137">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="f21ca-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="f21ca-138">System-Only</span></span>            | <span data-ttu-id="f21ca-139">False</span><span class="sxs-lookup"><span data-stu-id="f21ca-139">False</span></span>                                                                                                                       |
| <span data-ttu-id="f21ca-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f21ca-140">Is-Single-Valued</span></span>       | <span data-ttu-id="f21ca-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="f21ca-141">True</span></span>                                                                                                                        |
| <span data-ttu-id="f21ca-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f21ca-142">Is Indexed</span></span>             | <span data-ttu-id="f21ca-143">False</span><span class="sxs-lookup"><span data-stu-id="f21ca-143">False</span></span>                                                                                                                       |
| <span data-ttu-id="f21ca-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f21ca-144">In Global Catalog</span></span>      | <span data-ttu-id="f21ca-145">False</span><span class="sxs-lookup"><span data-stu-id="f21ca-145">False</span></span>                                                                                                                       |
| <span data-ttu-id="f21ca-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f21ca-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="f21ca-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f21ca-147">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="f21ca-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f21ca-148">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="f21ca-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f21ca-149">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="f21ca-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f21ca-150">Search-Flags</span></span>           | <span data-ttu-id="f21ca-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f21ca-151">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="f21ca-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f21ca-152">System-Flags</span></span>           | <span data-ttu-id="f21ca-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f21ca-153">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="f21ca-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f21ca-154">Classes used in</span></span>        | [<span data-ttu-id="f21ca-155">**MS-TAPI-RT-Konferenz**</span><span class="sxs-lookup"><span data-stu-id="f21ca-155">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="f21ca-156">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="f21ca-156">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f21ca-157">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f21ca-157">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f21ca-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f21ca-158">Entry</span></span> | <span data-ttu-id="f21ca-159">Wert</span><span class="sxs-lookup"><span data-stu-id="f21ca-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f21ca-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f21ca-160">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="f21ca-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f21ca-161">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="f21ca-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="f21ca-162">System-Only</span></span>            | <span data-ttu-id="f21ca-163">False</span><span class="sxs-lookup"><span data-stu-id="f21ca-163">False</span></span>                                                                                                                       |
| <span data-ttu-id="f21ca-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f21ca-164">Is-Single-Valued</span></span>       | <span data-ttu-id="f21ca-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="f21ca-165">True</span></span>                                                                                                                        |
| <span data-ttu-id="f21ca-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f21ca-166">Is Indexed</span></span>             | <span data-ttu-id="f21ca-167">False</span><span class="sxs-lookup"><span data-stu-id="f21ca-167">False</span></span>                                                                                                                       |
| <span data-ttu-id="f21ca-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f21ca-168">In Global Catalog</span></span>      | <span data-ttu-id="f21ca-169">False</span><span class="sxs-lookup"><span data-stu-id="f21ca-169">False</span></span>                                                                                                                       |
| <span data-ttu-id="f21ca-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f21ca-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="f21ca-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f21ca-171">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="f21ca-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f21ca-172">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="f21ca-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f21ca-173">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="f21ca-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f21ca-174">Search-Flags</span></span>           | <span data-ttu-id="f21ca-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f21ca-175">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="f21ca-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f21ca-176">System-Flags</span></span>           | <span data-ttu-id="f21ca-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f21ca-177">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="f21ca-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f21ca-178">Classes used in</span></span>        | [<span data-ttu-id="f21ca-179">**MS-TAPI-RT-Konferenz**</span><span class="sxs-lookup"><span data-stu-id="f21ca-179">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="f21ca-180">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="f21ca-180">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f21ca-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f21ca-181">Windows Server 2008</span></span>



| <span data-ttu-id="f21ca-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f21ca-182">Entry</span></span> | <span data-ttu-id="f21ca-183">Wert</span><span class="sxs-lookup"><span data-stu-id="f21ca-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f21ca-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f21ca-184">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="f21ca-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f21ca-185">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="f21ca-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="f21ca-186">System-Only</span></span>            | <span data-ttu-id="f21ca-187">False</span><span class="sxs-lookup"><span data-stu-id="f21ca-187">False</span></span>                                                                                                                       |
| <span data-ttu-id="f21ca-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f21ca-188">Is-Single-Valued</span></span>       | <span data-ttu-id="f21ca-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="f21ca-189">True</span></span>                                                                                                                        |
| <span data-ttu-id="f21ca-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f21ca-190">Is Indexed</span></span>             | <span data-ttu-id="f21ca-191">False</span><span class="sxs-lookup"><span data-stu-id="f21ca-191">False</span></span>                                                                                                                       |
| <span data-ttu-id="f21ca-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f21ca-192">In Global Catalog</span></span>      | <span data-ttu-id="f21ca-193">False</span><span class="sxs-lookup"><span data-stu-id="f21ca-193">False</span></span>                                                                                                                       |
| <span data-ttu-id="f21ca-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f21ca-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="f21ca-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f21ca-195">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="f21ca-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f21ca-196">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="f21ca-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f21ca-197">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="f21ca-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f21ca-198">Search-Flags</span></span>           | <span data-ttu-id="f21ca-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f21ca-199">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="f21ca-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f21ca-200">System-Flags</span></span>           | <span data-ttu-id="f21ca-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f21ca-201">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="f21ca-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f21ca-202">Classes used in</span></span>        | [<span data-ttu-id="f21ca-203">**MS-TAPI-RT-Konferenz**</span><span class="sxs-lookup"><span data-stu-id="f21ca-203">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="f21ca-204">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="f21ca-204">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f21ca-205">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f21ca-205">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f21ca-206">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f21ca-206">Entry</span></span> | <span data-ttu-id="f21ca-207">Wert</span><span class="sxs-lookup"><span data-stu-id="f21ca-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f21ca-208">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f21ca-208">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="f21ca-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f21ca-209">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="f21ca-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="f21ca-210">System-Only</span></span>            | <span data-ttu-id="f21ca-211">False</span><span class="sxs-lookup"><span data-stu-id="f21ca-211">False</span></span>                                                                                                                       |
| <span data-ttu-id="f21ca-212">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f21ca-212">Is-Single-Valued</span></span>       | <span data-ttu-id="f21ca-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="f21ca-213">True</span></span>                                                                                                                        |
| <span data-ttu-id="f21ca-214">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f21ca-214">Is Indexed</span></span>             | <span data-ttu-id="f21ca-215">False</span><span class="sxs-lookup"><span data-stu-id="f21ca-215">False</span></span>                                                                                                                       |
| <span data-ttu-id="f21ca-216">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f21ca-216">In Global Catalog</span></span>      | <span data-ttu-id="f21ca-217">False</span><span class="sxs-lookup"><span data-stu-id="f21ca-217">False</span></span>                                                                                                                       |
| <span data-ttu-id="f21ca-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f21ca-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="f21ca-219">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f21ca-219">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="f21ca-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f21ca-220">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="f21ca-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f21ca-221">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="f21ca-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f21ca-222">Search-Flags</span></span>           | <span data-ttu-id="f21ca-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f21ca-223">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="f21ca-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f21ca-224">System-Flags</span></span>           | <span data-ttu-id="f21ca-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f21ca-225">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="f21ca-226">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f21ca-226">Classes used in</span></span>        | [<span data-ttu-id="f21ca-227">**MS-TAPI-RT-Konferenz**</span><span class="sxs-lookup"><span data-stu-id="f21ca-227">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="f21ca-228">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="f21ca-228">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f21ca-229">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f21ca-229">Windows Server 2012</span></span>



| <span data-ttu-id="f21ca-230">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f21ca-230">Entry</span></span> | <span data-ttu-id="f21ca-231">Wert</span><span class="sxs-lookup"><span data-stu-id="f21ca-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f21ca-232">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f21ca-232">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="f21ca-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f21ca-233">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="f21ca-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="f21ca-234">System-Only</span></span>            | <span data-ttu-id="f21ca-235">False</span><span class="sxs-lookup"><span data-stu-id="f21ca-235">False</span></span>                                                                                                                       |
| <span data-ttu-id="f21ca-236">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f21ca-236">Is-Single-Valued</span></span>       | <span data-ttu-id="f21ca-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="f21ca-237">True</span></span>                                                                                                                        |
| <span data-ttu-id="f21ca-238">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f21ca-238">Is Indexed</span></span>             | <span data-ttu-id="f21ca-239">False</span><span class="sxs-lookup"><span data-stu-id="f21ca-239">False</span></span>                                                                                                                       |
| <span data-ttu-id="f21ca-240">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f21ca-240">In Global Catalog</span></span>      | <span data-ttu-id="f21ca-241">False</span><span class="sxs-lookup"><span data-stu-id="f21ca-241">False</span></span>                                                                                                                       |
| <span data-ttu-id="f21ca-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f21ca-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="f21ca-243">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f21ca-243">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="f21ca-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f21ca-244">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="f21ca-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f21ca-245">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="f21ca-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f21ca-246">Search-Flags</span></span>           | <span data-ttu-id="f21ca-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f21ca-247">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="f21ca-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f21ca-248">System-Flags</span></span>           | <span data-ttu-id="f21ca-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f21ca-249">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="f21ca-250">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f21ca-250">Classes used in</span></span>        | [<span data-ttu-id="f21ca-251">**MS-TAPI-RT-Konferenz**</span><span class="sxs-lookup"><span data-stu-id="f21ca-251">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="f21ca-252">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="f21ca-252">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



 

 





