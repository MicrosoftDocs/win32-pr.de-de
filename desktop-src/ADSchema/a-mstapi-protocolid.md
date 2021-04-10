---
title: MS-TAPI-Protocol-ID-Attribut
description: Dieses Attribut gibt den TAPI-Konferenztyp an.
ms.assetid: 6114efc3-4201-4f20-81ca-4f90a9e44f60
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-TAPI-Protocol-ID-Attributs
- MSTAPI-protokolid-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- ms-TAPI-Protocol-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10538f66b98988fafa69d4fe2f3e70b47348c999
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122834"
---
# <a name="ms-tapi-protocol-id-attribute"></a><span data-ttu-id="931eb-105">MS-TAPI-Protocol-ID-Attribut</span><span class="sxs-lookup"><span data-stu-id="931eb-105">ms-TAPI-Protocol-Id attribute</span></span>

<span data-ttu-id="931eb-106">Dieses Attribut gibt den TAPI-Konferenztyp an.</span><span class="sxs-lookup"><span data-stu-id="931eb-106">This attribute indicates the TAPI conference type.</span></span> <span data-ttu-id="931eb-107">Dieses Attribut wird verwendet, um zu bestimmen, wie das binäre Blob im [**MS-TAPI-Conference-BLOB-**](a-mstapi-conferenceblob.md) Attribut interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="931eb-107">This attribute is used to determine how the binary BLOB in the [**ms-TAPI-Conference-Blob**](a-mstapi-conferenceblob.md) attribute is to be interpreted.</span></span> <span data-ttu-id="931eb-108">Dieses Attribut ist eine beliebige Zeichenfolge, die in der Regel weniger als 100 Zeichen lang ist.</span><span class="sxs-lookup"><span data-stu-id="931eb-108">This attribute is an arbitrary string, typically less than 100 characters in length.</span></span>



| <span data-ttu-id="931eb-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="931eb-109">Entry</span></span> | <span data-ttu-id="931eb-110">Wert</span><span class="sxs-lookup"><span data-stu-id="931eb-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="931eb-111">CN</span><span class="sxs-lookup"><span data-stu-id="931eb-111">CN</span></span>                | <span data-ttu-id="931eb-112">MS-TAPI-Protocol-ID</span><span class="sxs-lookup"><span data-stu-id="931eb-112">ms-TAPI-Protocol-Id</span></span>                                        |
| <span data-ttu-id="931eb-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="931eb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="931eb-114">MSTAPI-protokolid</span><span class="sxs-lookup"><span data-stu-id="931eb-114">msTAPI-ProtocolId</span></span>                                          |
| <span data-ttu-id="931eb-115">Size</span><span class="sxs-lookup"><span data-stu-id="931eb-115">Size</span></span>              | \-                                                         |
| <span data-ttu-id="931eb-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="931eb-116">Update Privilege</span></span>  | <span data-ttu-id="931eb-117">Es sind keine besonderen Berechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="931eb-117">No special privileges required.</span></span>                            |
| <span data-ttu-id="931eb-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="931eb-118">Update Frequency</span></span>  | <span data-ttu-id="931eb-119">Wird einmal zum Zeitpunkt der Erstellung des Rt-Conference Objekts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="931eb-119">Set once at the time of creating the Rt-Conference object.</span></span> |
| <span data-ttu-id="931eb-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="931eb-120">Attribute-Id</span></span>      | <span data-ttu-id="931eb-121">1.2.840.113556.1.4.1699</span><span class="sxs-lookup"><span data-stu-id="931eb-121">1.2.840.113556.1.4.1699</span></span>                                    |
| <span data-ttu-id="931eb-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="931eb-122">System-Id-Guid</span></span>    | <span data-ttu-id="931eb-123">89c1ebcf-7a5f-41fd-99um-c900b32299ab</span><span class="sxs-lookup"><span data-stu-id="931eb-123">89c1ebcf-7a5f-41fd-99ca-c900b32299ab</span></span>                       |
| <span data-ttu-id="931eb-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="931eb-124">Syntax</span></span>            | [<span data-ttu-id="931eb-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="931eb-125">**String(Unicode)**</span></span>](s-string-unicode.md)                |



## <a name="implementations"></a><span data-ttu-id="931eb-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="931eb-126">Implementations</span></span>

-   [<span data-ttu-id="931eb-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="931eb-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="931eb-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="931eb-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="931eb-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="931eb-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="931eb-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="931eb-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="931eb-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="931eb-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="931eb-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="931eb-132">Windows Server 2003</span></span>



| <span data-ttu-id="931eb-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="931eb-133">Entry</span></span> | <span data-ttu-id="931eb-134">Wert</span><span class="sxs-lookup"><span data-stu-id="931eb-134">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="931eb-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="931eb-135">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="931eb-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="931eb-136">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="931eb-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="931eb-137">System-Only</span></span>            | <span data-ttu-id="931eb-138">False</span><span class="sxs-lookup"><span data-stu-id="931eb-138">False</span></span>                                                             |
| <span data-ttu-id="931eb-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="931eb-139">Is-Single-Valued</span></span>       | <span data-ttu-id="931eb-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="931eb-140">True</span></span>                                                              |
| <span data-ttu-id="931eb-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="931eb-141">Is Indexed</span></span>             | <span data-ttu-id="931eb-142">False</span><span class="sxs-lookup"><span data-stu-id="931eb-142">False</span></span>                                                             |
| <span data-ttu-id="931eb-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="931eb-143">In Global Catalog</span></span>      | <span data-ttu-id="931eb-144">False</span><span class="sxs-lookup"><span data-stu-id="931eb-144">False</span></span>                                                             |
| <span data-ttu-id="931eb-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="931eb-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="931eb-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="931eb-146">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="931eb-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="931eb-147">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="931eb-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="931eb-148">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="931eb-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="931eb-149">Search-Flags</span></span>           | <span data-ttu-id="931eb-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="931eb-150">0x00000000</span></span>                                                        |
| <span data-ttu-id="931eb-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="931eb-151">System-Flags</span></span>           | <span data-ttu-id="931eb-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="931eb-152">0x00000010</span></span>                                                        |
| <span data-ttu-id="931eb-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="931eb-153">Classes used in</span></span>        | [<span data-ttu-id="931eb-154">**MS-TAPI-RT-Konferenz**</span><span class="sxs-lookup"><span data-stu-id="931eb-154">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="931eb-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="931eb-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="931eb-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="931eb-156">Entry</span></span> | <span data-ttu-id="931eb-157">Wert</span><span class="sxs-lookup"><span data-stu-id="931eb-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="931eb-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="931eb-158">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="931eb-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="931eb-159">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="931eb-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="931eb-160">System-Only</span></span>            | <span data-ttu-id="931eb-161">False</span><span class="sxs-lookup"><span data-stu-id="931eb-161">False</span></span>                                                             |
| <span data-ttu-id="931eb-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="931eb-162">Is-Single-Valued</span></span>       | <span data-ttu-id="931eb-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="931eb-163">True</span></span>                                                              |
| <span data-ttu-id="931eb-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="931eb-164">Is Indexed</span></span>             | <span data-ttu-id="931eb-165">False</span><span class="sxs-lookup"><span data-stu-id="931eb-165">False</span></span>                                                             |
| <span data-ttu-id="931eb-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="931eb-166">In Global Catalog</span></span>      | <span data-ttu-id="931eb-167">False</span><span class="sxs-lookup"><span data-stu-id="931eb-167">False</span></span>                                                             |
| <span data-ttu-id="931eb-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="931eb-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="931eb-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="931eb-169">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="931eb-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="931eb-170">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="931eb-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="931eb-171">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="931eb-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="931eb-172">Search-Flags</span></span>           | <span data-ttu-id="931eb-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="931eb-173">0x00000000</span></span>                                                        |
| <span data-ttu-id="931eb-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="931eb-174">System-Flags</span></span>           | <span data-ttu-id="931eb-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="931eb-175">0x00000010</span></span>                                                        |
| <span data-ttu-id="931eb-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="931eb-176">Classes used in</span></span>        | [<span data-ttu-id="931eb-177">**MS-TAPI-RT-Konferenz**</span><span class="sxs-lookup"><span data-stu-id="931eb-177">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="931eb-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="931eb-178">Windows Server 2008</span></span>



| <span data-ttu-id="931eb-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="931eb-179">Entry</span></span> | <span data-ttu-id="931eb-180">Wert</span><span class="sxs-lookup"><span data-stu-id="931eb-180">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="931eb-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="931eb-181">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="931eb-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="931eb-182">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="931eb-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="931eb-183">System-Only</span></span>            | <span data-ttu-id="931eb-184">False</span><span class="sxs-lookup"><span data-stu-id="931eb-184">False</span></span>                                                             |
| <span data-ttu-id="931eb-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="931eb-185">Is-Single-Valued</span></span>       | <span data-ttu-id="931eb-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="931eb-186">True</span></span>                                                              |
| <span data-ttu-id="931eb-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="931eb-187">Is Indexed</span></span>             | <span data-ttu-id="931eb-188">False</span><span class="sxs-lookup"><span data-stu-id="931eb-188">False</span></span>                                                             |
| <span data-ttu-id="931eb-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="931eb-189">In Global Catalog</span></span>      | <span data-ttu-id="931eb-190">False</span><span class="sxs-lookup"><span data-stu-id="931eb-190">False</span></span>                                                             |
| <span data-ttu-id="931eb-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="931eb-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="931eb-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="931eb-192">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="931eb-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="931eb-193">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="931eb-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="931eb-194">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="931eb-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="931eb-195">Search-Flags</span></span>           | <span data-ttu-id="931eb-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="931eb-196">0x00000000</span></span>                                                        |
| <span data-ttu-id="931eb-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="931eb-197">System-Flags</span></span>           | <span data-ttu-id="931eb-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="931eb-198">0x00000010</span></span>                                                        |
| <span data-ttu-id="931eb-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="931eb-199">Classes used in</span></span>        | [<span data-ttu-id="931eb-200">**MS-TAPI-RT-Konferenz**</span><span class="sxs-lookup"><span data-stu-id="931eb-200">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="931eb-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="931eb-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="931eb-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="931eb-202">Entry</span></span> | <span data-ttu-id="931eb-203">Wert</span><span class="sxs-lookup"><span data-stu-id="931eb-203">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="931eb-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="931eb-204">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="931eb-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="931eb-205">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="931eb-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="931eb-206">System-Only</span></span>            | <span data-ttu-id="931eb-207">False</span><span class="sxs-lookup"><span data-stu-id="931eb-207">False</span></span>                                                             |
| <span data-ttu-id="931eb-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="931eb-208">Is-Single-Valued</span></span>       | <span data-ttu-id="931eb-209">Richtig</span><span class="sxs-lookup"><span data-stu-id="931eb-209">True</span></span>                                                              |
| <span data-ttu-id="931eb-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="931eb-210">Is Indexed</span></span>             | <span data-ttu-id="931eb-211">False</span><span class="sxs-lookup"><span data-stu-id="931eb-211">False</span></span>                                                             |
| <span data-ttu-id="931eb-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="931eb-212">In Global Catalog</span></span>      | <span data-ttu-id="931eb-213">False</span><span class="sxs-lookup"><span data-stu-id="931eb-213">False</span></span>                                                             |
| <span data-ttu-id="931eb-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="931eb-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="931eb-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="931eb-215">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="931eb-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="931eb-216">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="931eb-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="931eb-217">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="931eb-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="931eb-218">Search-Flags</span></span>           | <span data-ttu-id="931eb-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="931eb-219">0x00000000</span></span>                                                        |
| <span data-ttu-id="931eb-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="931eb-220">System-Flags</span></span>           | <span data-ttu-id="931eb-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="931eb-221">0x00000010</span></span>                                                        |
| <span data-ttu-id="931eb-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="931eb-222">Classes used in</span></span>        | [<span data-ttu-id="931eb-223">**MS-TAPI-RT-Konferenz**</span><span class="sxs-lookup"><span data-stu-id="931eb-223">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="931eb-224">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="931eb-224">Windows Server 2012</span></span>



| <span data-ttu-id="931eb-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="931eb-225">Entry</span></span> | <span data-ttu-id="931eb-226">Wert</span><span class="sxs-lookup"><span data-stu-id="931eb-226">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="931eb-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="931eb-227">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="931eb-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="931eb-228">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="931eb-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="931eb-229">System-Only</span></span>            | <span data-ttu-id="931eb-230">False</span><span class="sxs-lookup"><span data-stu-id="931eb-230">False</span></span>                                                             |
| <span data-ttu-id="931eb-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="931eb-231">Is-Single-Valued</span></span>       | <span data-ttu-id="931eb-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="931eb-232">True</span></span>                                                              |
| <span data-ttu-id="931eb-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="931eb-233">Is Indexed</span></span>             | <span data-ttu-id="931eb-234">False</span><span class="sxs-lookup"><span data-stu-id="931eb-234">False</span></span>                                                             |
| <span data-ttu-id="931eb-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="931eb-235">In Global Catalog</span></span>      | <span data-ttu-id="931eb-236">False</span><span class="sxs-lookup"><span data-stu-id="931eb-236">False</span></span>                                                             |
| <span data-ttu-id="931eb-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="931eb-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="931eb-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="931eb-238">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="931eb-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="931eb-239">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="931eb-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="931eb-240">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="931eb-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="931eb-241">Search-Flags</span></span>           | <span data-ttu-id="931eb-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="931eb-242">0x00000000</span></span>                                                        |
| <span data-ttu-id="931eb-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="931eb-243">System-Flags</span></span>           | <span data-ttu-id="931eb-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="931eb-244">0x00000010</span></span>                                                        |
| <span data-ttu-id="931eb-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="931eb-245">Classes used in</span></span>        | [<span data-ttu-id="931eb-246">**MS-TAPI-RT-Konferenz**</span><span class="sxs-lookup"><span data-stu-id="931eb-246">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



 

 





