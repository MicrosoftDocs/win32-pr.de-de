---
title: MS-TAPI-IP-address-Attribut
description: IP-Adressen eines TAPI-Client Computers, bei dem ein Benutzer angemeldet ist. Dieses Attribut kann als generisches Attribut für Computer-IP-Adressen verwendet werden.
ms.assetid: 4ea850ad-d54a-4b5f-a37d-68817432d874
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-TAPI-IP-address-Attribut
- MSTAPI-IPAddress-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-TAPI-Ip-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078afde8200468df7e996e096deeef4bfd1b7ec0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957483"
---
# <a name="ms-tapi-ip-address-attribute"></a><span data-ttu-id="a8169-106">MS-TAPI-IP-address-Attribut</span><span class="sxs-lookup"><span data-stu-id="a8169-106">ms-TAPI-Ip-Address attribute</span></span>

<span data-ttu-id="a8169-107">IP-Adressen eines TAPI-Client Computers, bei dem ein Benutzer angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="a8169-107">IP addresses of a TAPI client computer that a user is logged into.</span></span> <span data-ttu-id="a8169-108">Dieses Attribut kann als generisches Attribut für Computer-IP-Adressen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a8169-108">This attribute can be used as a generic attribute to hold computer IP addresses.</span></span>



| <span data-ttu-id="a8169-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8169-109">Entry</span></span> | <span data-ttu-id="a8169-110">Wert</span><span class="sxs-lookup"><span data-stu-id="a8169-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="a8169-111">CN</span><span class="sxs-lookup"><span data-stu-id="a8169-111">CN</span></span>                | <span data-ttu-id="a8169-112">MS-TAPI-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="a8169-112">ms-TAPI-Ip-Address</span></span>                                         |
| <span data-ttu-id="a8169-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a8169-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a8169-114">MSTAPI-IPAddress</span><span class="sxs-lookup"><span data-stu-id="a8169-114">msTAPI-IpAddress</span></span>                                           |
| <span data-ttu-id="a8169-115">Size</span><span class="sxs-lookup"><span data-stu-id="a8169-115">Size</span></span>              | <span data-ttu-id="a8169-116">Jede IP-Adresse wird als Zeichenfolge in einer. B. C. D-Notation gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a8169-116">Each IP address is stored as a string in A.B.C.D notation.</span></span> |
| <span data-ttu-id="a8169-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a8169-117">Update Privilege</span></span>  | <span data-ttu-id="a8169-118">Es sind keine besonderen Berechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a8169-118">No special privileges required.</span></span>                            |
| <span data-ttu-id="a8169-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="a8169-119">Update Frequency</span></span>  | <span data-ttu-id="a8169-120">Normalerweise sehr niedrig.</span><span class="sxs-lookup"><span data-stu-id="a8169-120">Typically very low.</span></span>                                        |
| <span data-ttu-id="a8169-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a8169-121">Attribute-Id</span></span>      | <span data-ttu-id="a8169-122">1.2.840.113556.1.4.1701</span><span class="sxs-lookup"><span data-stu-id="a8169-122">1.2.840.113556.1.4.1701</span></span>                                    |
| <span data-ttu-id="a8169-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a8169-123">System-Id-Guid</span></span>    | <span data-ttu-id="a8169-124">efd7d7f7-178e-4767-87fa-f8a16b840544</span><span class="sxs-lookup"><span data-stu-id="a8169-124">efd7d7f7-178e-4767-87fa-f8a16b840544</span></span>                       |
| <span data-ttu-id="a8169-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8169-125">Syntax</span></span>            | [<span data-ttu-id="a8169-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a8169-126">**String(Unicode)**</span></span>](s-string-unicode.md)                |



## <a name="implementations"></a><span data-ttu-id="a8169-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="a8169-127">Implementations</span></span>

-   [<span data-ttu-id="a8169-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a8169-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a8169-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a8169-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a8169-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a8169-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a8169-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a8169-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a8169-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a8169-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a8169-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8169-133">Windows Server 2003</span></span>



| <span data-ttu-id="a8169-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8169-134">Entry</span></span> | <span data-ttu-id="a8169-135">Wert</span><span class="sxs-lookup"><span data-stu-id="a8169-135">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a8169-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8169-136">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a8169-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8169-137">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a8169-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8169-138">System-Only</span></span>            | <span data-ttu-id="a8169-139">False</span><span class="sxs-lookup"><span data-stu-id="a8169-139">False</span></span>                                                     |
| <span data-ttu-id="a8169-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8169-140">Is-Single-Valued</span></span>       | <span data-ttu-id="a8169-141">False</span><span class="sxs-lookup"><span data-stu-id="a8169-141">False</span></span>                                                     |
| <span data-ttu-id="a8169-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8169-142">Is Indexed</span></span>             | <span data-ttu-id="a8169-143">False</span><span class="sxs-lookup"><span data-stu-id="a8169-143">False</span></span>                                                     |
| <span data-ttu-id="a8169-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8169-144">In Global Catalog</span></span>      | <span data-ttu-id="a8169-145">False</span><span class="sxs-lookup"><span data-stu-id="a8169-145">False</span></span>                                                     |
| <span data-ttu-id="a8169-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8169-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8169-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8169-147">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a8169-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8169-148">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a8169-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8169-149">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a8169-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8169-150">Search-Flags</span></span>           | <span data-ttu-id="a8169-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8169-151">0x00000000</span></span>                                                |
| <span data-ttu-id="a8169-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8169-152">System-Flags</span></span>           | <span data-ttu-id="a8169-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8169-153">0x00000010</span></span>                                                |
| <span data-ttu-id="a8169-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8169-154">Classes used in</span></span>        | [<span data-ttu-id="a8169-155">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="a8169-155">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a8169-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a8169-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a8169-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8169-157">Entry</span></span> | <span data-ttu-id="a8169-158">Wert</span><span class="sxs-lookup"><span data-stu-id="a8169-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a8169-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8169-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a8169-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8169-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a8169-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8169-161">System-Only</span></span>            | <span data-ttu-id="a8169-162">False</span><span class="sxs-lookup"><span data-stu-id="a8169-162">False</span></span>                                                     |
| <span data-ttu-id="a8169-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8169-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a8169-164">False</span><span class="sxs-lookup"><span data-stu-id="a8169-164">False</span></span>                                                     |
| <span data-ttu-id="a8169-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8169-165">Is Indexed</span></span>             | <span data-ttu-id="a8169-166">False</span><span class="sxs-lookup"><span data-stu-id="a8169-166">False</span></span>                                                     |
| <span data-ttu-id="a8169-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8169-167">In Global Catalog</span></span>      | <span data-ttu-id="a8169-168">False</span><span class="sxs-lookup"><span data-stu-id="a8169-168">False</span></span>                                                     |
| <span data-ttu-id="a8169-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8169-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8169-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8169-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a8169-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8169-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a8169-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8169-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a8169-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8169-173">Search-Flags</span></span>           | <span data-ttu-id="a8169-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8169-174">0x00000000</span></span>                                                |
| <span data-ttu-id="a8169-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8169-175">System-Flags</span></span>           | <span data-ttu-id="a8169-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8169-176">0x00000010</span></span>                                                |
| <span data-ttu-id="a8169-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8169-177">Classes used in</span></span>        | [<span data-ttu-id="a8169-178">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="a8169-178">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a8169-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8169-179">Windows Server 2008</span></span>



| <span data-ttu-id="a8169-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8169-180">Entry</span></span> | <span data-ttu-id="a8169-181">Wert</span><span class="sxs-lookup"><span data-stu-id="a8169-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a8169-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8169-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a8169-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8169-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a8169-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8169-184">System-Only</span></span>            | <span data-ttu-id="a8169-185">False</span><span class="sxs-lookup"><span data-stu-id="a8169-185">False</span></span>                                                     |
| <span data-ttu-id="a8169-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8169-186">Is-Single-Valued</span></span>       | <span data-ttu-id="a8169-187">False</span><span class="sxs-lookup"><span data-stu-id="a8169-187">False</span></span>                                                     |
| <span data-ttu-id="a8169-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8169-188">Is Indexed</span></span>             | <span data-ttu-id="a8169-189">False</span><span class="sxs-lookup"><span data-stu-id="a8169-189">False</span></span>                                                     |
| <span data-ttu-id="a8169-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8169-190">In Global Catalog</span></span>      | <span data-ttu-id="a8169-191">False</span><span class="sxs-lookup"><span data-stu-id="a8169-191">False</span></span>                                                     |
| <span data-ttu-id="a8169-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8169-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8169-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8169-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a8169-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8169-194">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a8169-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8169-195">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a8169-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8169-196">Search-Flags</span></span>           | <span data-ttu-id="a8169-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8169-197">0x00000000</span></span>                                                |
| <span data-ttu-id="a8169-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8169-198">System-Flags</span></span>           | <span data-ttu-id="a8169-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8169-199">0x00000010</span></span>                                                |
| <span data-ttu-id="a8169-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8169-200">Classes used in</span></span>        | [<span data-ttu-id="a8169-201">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="a8169-201">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a8169-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a8169-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a8169-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8169-203">Entry</span></span> | <span data-ttu-id="a8169-204">Wert</span><span class="sxs-lookup"><span data-stu-id="a8169-204">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a8169-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8169-205">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a8169-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8169-206">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a8169-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8169-207">System-Only</span></span>            | <span data-ttu-id="a8169-208">False</span><span class="sxs-lookup"><span data-stu-id="a8169-208">False</span></span>                                                     |
| <span data-ttu-id="a8169-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8169-209">Is-Single-Valued</span></span>       | <span data-ttu-id="a8169-210">False</span><span class="sxs-lookup"><span data-stu-id="a8169-210">False</span></span>                                                     |
| <span data-ttu-id="a8169-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8169-211">Is Indexed</span></span>             | <span data-ttu-id="a8169-212">False</span><span class="sxs-lookup"><span data-stu-id="a8169-212">False</span></span>                                                     |
| <span data-ttu-id="a8169-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8169-213">In Global Catalog</span></span>      | <span data-ttu-id="a8169-214">False</span><span class="sxs-lookup"><span data-stu-id="a8169-214">False</span></span>                                                     |
| <span data-ttu-id="a8169-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8169-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8169-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8169-216">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a8169-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8169-217">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a8169-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8169-218">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a8169-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8169-219">Search-Flags</span></span>           | <span data-ttu-id="a8169-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8169-220">0x00000000</span></span>                                                |
| <span data-ttu-id="a8169-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8169-221">System-Flags</span></span>           | <span data-ttu-id="a8169-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8169-222">0x00000010</span></span>                                                |
| <span data-ttu-id="a8169-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8169-223">Classes used in</span></span>        | [<span data-ttu-id="a8169-224">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="a8169-224">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a8169-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a8169-225">Windows Server 2012</span></span>



| <span data-ttu-id="a8169-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a8169-226">Entry</span></span> | <span data-ttu-id="a8169-227">Wert</span><span class="sxs-lookup"><span data-stu-id="a8169-227">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a8169-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a8169-228">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a8169-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8169-229">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a8169-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8169-230">System-Only</span></span>            | <span data-ttu-id="a8169-231">False</span><span class="sxs-lookup"><span data-stu-id="a8169-231">False</span></span>                                                     |
| <span data-ttu-id="a8169-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a8169-232">Is-Single-Valued</span></span>       | <span data-ttu-id="a8169-233">False</span><span class="sxs-lookup"><span data-stu-id="a8169-233">False</span></span>                                                     |
| <span data-ttu-id="a8169-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a8169-234">Is Indexed</span></span>             | <span data-ttu-id="a8169-235">False</span><span class="sxs-lookup"><span data-stu-id="a8169-235">False</span></span>                                                     |
| <span data-ttu-id="a8169-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a8169-236">In Global Catalog</span></span>      | <span data-ttu-id="a8169-237">False</span><span class="sxs-lookup"><span data-stu-id="a8169-237">False</span></span>                                                     |
| <span data-ttu-id="a8169-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8169-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8169-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a8169-239">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a8169-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8169-240">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a8169-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8169-241">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a8169-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8169-242">Search-Flags</span></span>           | <span data-ttu-id="a8169-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8169-243">0x00000000</span></span>                                                |
| <span data-ttu-id="a8169-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8169-244">System-Flags</span></span>           | <span data-ttu-id="a8169-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8169-245">0x00000010</span></span>                                                |
| <span data-ttu-id="a8169-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a8169-246">Classes used in</span></span>        | [<span data-ttu-id="a8169-247">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="a8169-247">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



 

 





