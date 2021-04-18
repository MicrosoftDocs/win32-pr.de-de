---
title: Attribut "in-Address-Book" anzeigen
description: Mit diesem Attribut wird angegeben, in welchen MAPI-Adressbüchern ein Objekt angezeigt wird.
ms.assetid: de00da4d-7c04-4d1d-b375-ce3b5eb2f50f
ms.tgt_platform: multiple
keywords:
- AD-Schema für das Show-in-Address-Book-Attribut
- AD-Schema für showInAddressBook-Attribut
topic_type:
- apiref
api_name:
- Show-In-Address-Book
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44632604c539278c67e9dd46537d8e797e2d70d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479927"
---
# <a name="show-in-address-book-attribute"></a><span data-ttu-id="6ac3a-105">Attribut "in-Address-Book" anzeigen</span><span class="sxs-lookup"><span data-stu-id="6ac3a-105">Show-In-Address-Book attribute</span></span>

<span data-ttu-id="6ac3a-106">Mit diesem Attribut wird angegeben, in welchen MAPI-Adressbüchern ein Objekt angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-106">This attribute is used to indicate in which MAPI address books an object will appear.</span></span> <span data-ttu-id="6ac3a-107">Sie wird normalerweise vom Exchange-Empfänger Aktualisierungs Dienst verwaltet.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-107">It is usually maintained by the Exchange Recipient Update Service.</span></span>



| <span data-ttu-id="6ac3a-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6ac3a-108">Entry</span></span> | <span data-ttu-id="6ac3a-109">Wert</span><span class="sxs-lookup"><span data-stu-id="6ac3a-109">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="6ac3a-110">CN</span><span class="sxs-lookup"><span data-stu-id="6ac3a-110">CN</span></span>                | <span data-ttu-id="6ac3a-111">In-Address-Book anzeigen</span><span class="sxs-lookup"><span data-stu-id="6ac3a-111">Show-In-Address-Book</span></span>                    |
| <span data-ttu-id="6ac3a-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6ac3a-112">Ldap-Display-Name</span></span> | <span data-ttu-id="6ac3a-113">showInAddressBook</span><span class="sxs-lookup"><span data-stu-id="6ac3a-113">showInAddressBook</span></span>                       |
| <span data-ttu-id="6ac3a-114">Size</span><span class="sxs-lookup"><span data-stu-id="6ac3a-114">Size</span></span>              | \-                                      |
| <span data-ttu-id="6ac3a-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="6ac3a-115">Update Privilege</span></span>  | <span data-ttu-id="6ac3a-116">Diese wird vom System verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-116">This is used by the system.</span></span>             |
| <span data-ttu-id="6ac3a-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="6ac3a-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="6ac3a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6ac3a-118">Attribute-Id</span></span>      | <span data-ttu-id="6ac3a-119">1.2.840.113556.1.4.644</span><span class="sxs-lookup"><span data-stu-id="6ac3a-119">1.2.840.113556.1.4.644</span></span>                  |
| <span data-ttu-id="6ac3a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6ac3a-120">System-Id-Guid</span></span>    | <span data-ttu-id="6ac3a-121">3e74f 60E-3e73-11d1-a9c0-0000e80367c1</span><span class="sxs-lookup"><span data-stu-id="6ac3a-121">3e74f60e-3e73-11d1-a9c0-0000f80367c1</span></span>    |
| <span data-ttu-id="6ac3a-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ac3a-122">Syntax</span></span>            | [<span data-ttu-id="6ac3a-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="6ac3a-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="6ac3a-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="6ac3a-124">Implementations</span></span>

-   [<span data-ttu-id="6ac3a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6ac3a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6ac3a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6ac3a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6ac3a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6ac3a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6ac3a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6ac3a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6ac3a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6ac3a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6ac3a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6ac3a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6ac3a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6ac3a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6ac3a-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6ac3a-132">Entry</span></span> | <span data-ttu-id="6ac3a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="6ac3a-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6ac3a-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6ac3a-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6ac3a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ac3a-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6ac3a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ac3a-136">System-Only</span></span>            | <span data-ttu-id="6ac3a-137">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-137">False</span></span>                                                |
| <span data-ttu-id="6ac3a-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6ac3a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6ac3a-139">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-139">False</span></span>                                                |
| <span data-ttu-id="6ac3a-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6ac3a-140">Is Indexed</span></span>             | <span data-ttu-id="6ac3a-141">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-141">False</span></span>                                                |
| <span data-ttu-id="6ac3a-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6ac3a-142">In Global Catalog</span></span>      | <span data-ttu-id="6ac3a-143">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-143">False</span></span>                                                |
| <span data-ttu-id="6ac3a-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6ac3a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ac3a-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6ac3a-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6ac3a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ac3a-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6ac3a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ac3a-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6ac3a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ac3a-148">Search-Flags</span></span>           | <span data-ttu-id="6ac3a-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ac3a-149">0x00000010</span></span>                                           |
| <span data-ttu-id="6ac3a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ac3a-150">System-Flags</span></span>           | <span data-ttu-id="6ac3a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ac3a-151">0x00000010</span></span>                                           |
| <span data-ttu-id="6ac3a-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6ac3a-152">Classes used in</span></span>        | [<span data-ttu-id="6ac3a-153">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="6ac3a-153">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6ac3a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6ac3a-154">Windows Server 2003</span></span>



| <span data-ttu-id="6ac3a-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6ac3a-155">Entry</span></span> | <span data-ttu-id="6ac3a-156">Wert</span><span class="sxs-lookup"><span data-stu-id="6ac3a-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6ac3a-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6ac3a-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6ac3a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ac3a-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6ac3a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ac3a-159">System-Only</span></span>            | <span data-ttu-id="6ac3a-160">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-160">False</span></span>                                                |
| <span data-ttu-id="6ac3a-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6ac3a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="6ac3a-162">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-162">False</span></span>                                                |
| <span data-ttu-id="6ac3a-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6ac3a-163">Is Indexed</span></span>             | <span data-ttu-id="6ac3a-164">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-164">False</span></span>                                                |
| <span data-ttu-id="6ac3a-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6ac3a-165">In Global Catalog</span></span>      | <span data-ttu-id="6ac3a-166">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-166">False</span></span>                                                |
| <span data-ttu-id="6ac3a-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6ac3a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ac3a-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6ac3a-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6ac3a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ac3a-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6ac3a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ac3a-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6ac3a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ac3a-171">Search-Flags</span></span>           | <span data-ttu-id="6ac3a-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ac3a-172">0x00000010</span></span>                                           |
| <span data-ttu-id="6ac3a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ac3a-173">System-Flags</span></span>           | <span data-ttu-id="6ac3a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ac3a-174">0x00000010</span></span>                                           |
| <span data-ttu-id="6ac3a-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6ac3a-175">Classes used in</span></span>        | [<span data-ttu-id="6ac3a-176">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="6ac3a-176">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6ac3a-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6ac3a-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6ac3a-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6ac3a-178">Entry</span></span> | <span data-ttu-id="6ac3a-179">Wert</span><span class="sxs-lookup"><span data-stu-id="6ac3a-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6ac3a-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6ac3a-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6ac3a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ac3a-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6ac3a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ac3a-182">System-Only</span></span>            | <span data-ttu-id="6ac3a-183">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-183">False</span></span>                                                |
| <span data-ttu-id="6ac3a-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6ac3a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="6ac3a-185">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-185">False</span></span>                                                |
| <span data-ttu-id="6ac3a-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6ac3a-186">Is Indexed</span></span>             | <span data-ttu-id="6ac3a-187">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-187">False</span></span>                                                |
| <span data-ttu-id="6ac3a-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6ac3a-188">In Global Catalog</span></span>      | <span data-ttu-id="6ac3a-189">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-189">False</span></span>                                                |
| <span data-ttu-id="6ac3a-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6ac3a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ac3a-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6ac3a-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6ac3a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ac3a-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6ac3a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ac3a-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6ac3a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ac3a-194">Search-Flags</span></span>           | <span data-ttu-id="6ac3a-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ac3a-195">0x00000010</span></span>                                           |
| <span data-ttu-id="6ac3a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ac3a-196">System-Flags</span></span>           | <span data-ttu-id="6ac3a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ac3a-197">0x00000010</span></span>                                           |
| <span data-ttu-id="6ac3a-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6ac3a-198">Classes used in</span></span>        | [<span data-ttu-id="6ac3a-199">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="6ac3a-199">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6ac3a-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ac3a-200">Windows Server 2008</span></span>



| <span data-ttu-id="6ac3a-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6ac3a-201">Entry</span></span> | <span data-ttu-id="6ac3a-202">Wert</span><span class="sxs-lookup"><span data-stu-id="6ac3a-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6ac3a-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6ac3a-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6ac3a-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ac3a-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6ac3a-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ac3a-205">System-Only</span></span>            | <span data-ttu-id="6ac3a-206">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-206">False</span></span>                                                |
| <span data-ttu-id="6ac3a-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6ac3a-207">Is-Single-Valued</span></span>       | <span data-ttu-id="6ac3a-208">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-208">False</span></span>                                                |
| <span data-ttu-id="6ac3a-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6ac3a-209">Is Indexed</span></span>             | <span data-ttu-id="6ac3a-210">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-210">False</span></span>                                                |
| <span data-ttu-id="6ac3a-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6ac3a-211">In Global Catalog</span></span>      | <span data-ttu-id="6ac3a-212">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-212">False</span></span>                                                |
| <span data-ttu-id="6ac3a-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6ac3a-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ac3a-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6ac3a-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6ac3a-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ac3a-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6ac3a-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ac3a-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6ac3a-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ac3a-217">Search-Flags</span></span>           | <span data-ttu-id="6ac3a-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ac3a-218">0x00000010</span></span>                                           |
| <span data-ttu-id="6ac3a-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ac3a-219">System-Flags</span></span>           | <span data-ttu-id="6ac3a-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ac3a-220">0x00000010</span></span>                                           |
| <span data-ttu-id="6ac3a-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6ac3a-221">Classes used in</span></span>        | [<span data-ttu-id="6ac3a-222">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="6ac3a-222">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6ac3a-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6ac3a-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6ac3a-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6ac3a-224">Entry</span></span> | <span data-ttu-id="6ac3a-225">Wert</span><span class="sxs-lookup"><span data-stu-id="6ac3a-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6ac3a-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6ac3a-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6ac3a-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ac3a-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6ac3a-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ac3a-228">System-Only</span></span>            | <span data-ttu-id="6ac3a-229">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-229">False</span></span>                                                |
| <span data-ttu-id="6ac3a-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6ac3a-230">Is-Single-Valued</span></span>       | <span data-ttu-id="6ac3a-231">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-231">False</span></span>                                                |
| <span data-ttu-id="6ac3a-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6ac3a-232">Is Indexed</span></span>             | <span data-ttu-id="6ac3a-233">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-233">False</span></span>                                                |
| <span data-ttu-id="6ac3a-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6ac3a-234">In Global Catalog</span></span>      | <span data-ttu-id="6ac3a-235">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-235">False</span></span>                                                |
| <span data-ttu-id="6ac3a-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6ac3a-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ac3a-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6ac3a-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6ac3a-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ac3a-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6ac3a-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ac3a-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6ac3a-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ac3a-240">Search-Flags</span></span>           | <span data-ttu-id="6ac3a-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ac3a-241">0x00000010</span></span>                                           |
| <span data-ttu-id="6ac3a-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ac3a-242">System-Flags</span></span>           | <span data-ttu-id="6ac3a-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ac3a-243">0x00000010</span></span>                                           |
| <span data-ttu-id="6ac3a-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6ac3a-244">Classes used in</span></span>        | [<span data-ttu-id="6ac3a-245">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="6ac3a-245">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6ac3a-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6ac3a-246">Windows Server 2012</span></span>



| <span data-ttu-id="6ac3a-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6ac3a-247">Entry</span></span> | <span data-ttu-id="6ac3a-248">Wert</span><span class="sxs-lookup"><span data-stu-id="6ac3a-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="6ac3a-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6ac3a-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6ac3a-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ac3a-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="6ac3a-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ac3a-251">System-Only</span></span>            | <span data-ttu-id="6ac3a-252">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-252">False</span></span>                                                |
| <span data-ttu-id="6ac3a-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6ac3a-253">Is-Single-Valued</span></span>       | <span data-ttu-id="6ac3a-254">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-254">False</span></span>                                                |
| <span data-ttu-id="6ac3a-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6ac3a-255">Is Indexed</span></span>             | <span data-ttu-id="6ac3a-256">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-256">False</span></span>                                                |
| <span data-ttu-id="6ac3a-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6ac3a-257">In Global Catalog</span></span>      | <span data-ttu-id="6ac3a-258">False</span><span class="sxs-lookup"><span data-stu-id="6ac3a-258">False</span></span>                                                |
| <span data-ttu-id="6ac3a-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6ac3a-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ac3a-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6ac3a-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="6ac3a-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ac3a-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="6ac3a-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ac3a-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="6ac3a-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ac3a-263">Search-Flags</span></span>           | <span data-ttu-id="6ac3a-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ac3a-264">0x00000010</span></span>                                           |
| <span data-ttu-id="6ac3a-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ac3a-265">System-Flags</span></span>           | <span data-ttu-id="6ac3a-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ac3a-266">0x00000010</span></span>                                           |
| <span data-ttu-id="6ac3a-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6ac3a-267">Classes used in</span></span>        | [<span data-ttu-id="6ac3a-268">**E-Mail-Empfänger**</span><span class="sxs-lookup"><span data-stu-id="6ac3a-268">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 





