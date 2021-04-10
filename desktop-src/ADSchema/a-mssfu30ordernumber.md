---
title: msSFU-30-Order-Number-Attribut
description: Enthält einen Wert, der von NIS verwendet wird, um zu überprüfen, ob sich die Zuordnung geändert hat.
ms.assetid: b2e83980-2de4-4001-b65a-8073c9258b27
ms.tgt_platform: multiple
keywords:
- msSFU-30-Order-Number-Attribut, AD-Schema
- msSFU30OrderNumber-Attribut AD-Schema
topic_type:
- apiref
api_name:
- msSFU-30-Order-Number
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af67f1b5d6fdff8ca4a7739276443d67fa35679f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107703"
---
# <a name="mssfu-30-order-number-attribute"></a><span data-ttu-id="9a969-105">msSFU-30-Order-Number-Attribut</span><span class="sxs-lookup"><span data-stu-id="9a969-105">msSFU-30-Order-Number attribute</span></span>

<span data-ttu-id="9a969-106">Enthält einen Wert, der von NIS verwendet wird, um zu überprüfen, ob sich die Zuordnung geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9a969-106">Contains a value that is used by NIS to check if the map has changed.</span></span> <span data-ttu-id="9a969-107">Jedes Mal, wenn die im [**msSFU-30-Domain-Info**](c-mssfu30domaininfo.md) -Objekt gespeicherten Daten geändert werden, wird dieser Wert inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="9a969-107">Every time the data stored in the [**msSFU-30-Domain-Info**](c-mssfu30domaininfo.md) object changes, this value is incremented.</span></span> <span data-ttu-id="9a969-108">Dieser Wert wird verwendet, um Datenänderungen zwischen **ypxfer** -aufrufen zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="9a969-108">This value is used to track data changes between **ypxfer** calls.</span></span>



| <span data-ttu-id="9a969-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a969-109">Entry</span></span> | <span data-ttu-id="9a969-110">Wert</span><span class="sxs-lookup"><span data-stu-id="9a969-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9a969-111">CN</span><span class="sxs-lookup"><span data-stu-id="9a969-111">CN</span></span>                | <span data-ttu-id="9a969-112">msSFU-30-Bestellnummer</span><span class="sxs-lookup"><span data-stu-id="9a969-112">msSFU-30-Order-Number</span></span>                       |
| <span data-ttu-id="9a969-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9a969-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9a969-114">msSFU30OrderNumber</span><span class="sxs-lookup"><span data-stu-id="9a969-114">msSFU30OrderNumber</span></span>                          |
| <span data-ttu-id="9a969-115">Size</span><span class="sxs-lookup"><span data-stu-id="9a969-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="9a969-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="9a969-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="9a969-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="9a969-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="9a969-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9a969-118">Attribute-Id</span></span>      | <span data-ttu-id="9a969-119">1.2.840.113556.1.6.18.1.308</span><span class="sxs-lookup"><span data-stu-id="9a969-119">1.2.840.113556.1.6.18.1.308</span></span>                 |
| <span data-ttu-id="9a969-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9a969-120">System-Id-Guid</span></span>    | <span data-ttu-id="9a969-121">02625f 05-d1ee-4f-b366-55266becb95c</span><span class="sxs-lookup"><span data-stu-id="9a969-121">02625f05-d1ee-4f9f-b366-55266becb95c</span></span>        |
| <span data-ttu-id="9a969-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a969-122">Syntax</span></span>            | [<span data-ttu-id="9a969-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9a969-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9a969-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="9a969-124">Implementations</span></span>

-   [<span data-ttu-id="9a969-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9a969-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9a969-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9a969-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9a969-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9a969-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9a969-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9a969-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003-r2"></a><span data-ttu-id="9a969-129">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9a969-129">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9a969-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a969-130">Entry</span></span> | <span data-ttu-id="9a969-131">Wert</span><span class="sxs-lookup"><span data-stu-id="9a969-131">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9a969-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a969-132">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9a969-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a969-133">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9a969-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a969-134">System-Only</span></span>            | <span data-ttu-id="9a969-135">False</span><span class="sxs-lookup"><span data-stu-id="9a969-135">False</span></span>                                                          |
| <span data-ttu-id="9a969-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a969-136">Is-Single-Valued</span></span>       | <span data-ttu-id="9a969-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a969-137">True</span></span>                                                           |
| <span data-ttu-id="9a969-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a969-138">Is Indexed</span></span>             | <span data-ttu-id="9a969-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a969-139">True</span></span>                                                           |
| <span data-ttu-id="9a969-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a969-140">In Global Catalog</span></span>      | <span data-ttu-id="9a969-141">False</span><span class="sxs-lookup"><span data-stu-id="9a969-141">False</span></span>                                                          |
| <span data-ttu-id="9a969-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a969-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a969-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a969-143">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9a969-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a969-144">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="9a969-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a969-145">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="9a969-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a969-146">Search-Flags</span></span>           | <span data-ttu-id="9a969-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9a969-147">0x00000001</span></span>                                                     |
| <span data-ttu-id="9a969-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a969-148">System-Flags</span></span>           | <span data-ttu-id="9a969-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a969-149">0x00000000</span></span>                                                     |
| <span data-ttu-id="9a969-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a969-150">Classes used in</span></span>        | [<span data-ttu-id="9a969-151">**msSFU-30-Domäne-Info**</span><span class="sxs-lookup"><span data-stu-id="9a969-151">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9a969-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a969-152">Windows Server 2008</span></span>



| <span data-ttu-id="9a969-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a969-153">Entry</span></span> | <span data-ttu-id="9a969-154">Wert</span><span class="sxs-lookup"><span data-stu-id="9a969-154">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9a969-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a969-155">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9a969-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a969-156">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9a969-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a969-157">System-Only</span></span>            | <span data-ttu-id="9a969-158">False</span><span class="sxs-lookup"><span data-stu-id="9a969-158">False</span></span>                                                          |
| <span data-ttu-id="9a969-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a969-159">Is-Single-Valued</span></span>       | <span data-ttu-id="9a969-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a969-160">True</span></span>                                                           |
| <span data-ttu-id="9a969-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a969-161">Is Indexed</span></span>             | <span data-ttu-id="9a969-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a969-162">True</span></span>                                                           |
| <span data-ttu-id="9a969-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a969-163">In Global Catalog</span></span>      | <span data-ttu-id="9a969-164">False</span><span class="sxs-lookup"><span data-stu-id="9a969-164">False</span></span>                                                          |
| <span data-ttu-id="9a969-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a969-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a969-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a969-166">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9a969-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a969-167">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="9a969-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a969-168">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="9a969-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a969-169">Search-Flags</span></span>           | <span data-ttu-id="9a969-170">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9a969-170">0x00000001</span></span>                                                     |
| <span data-ttu-id="9a969-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a969-171">System-Flags</span></span>           | <span data-ttu-id="9a969-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a969-172">0x00000000</span></span>                                                     |
| <span data-ttu-id="9a969-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a969-173">Classes used in</span></span>        | [<span data-ttu-id="9a969-174">**msSFU-30-Domäne-Info**</span><span class="sxs-lookup"><span data-stu-id="9a969-174">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9a969-175">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9a969-175">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9a969-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a969-176">Entry</span></span> | <span data-ttu-id="9a969-177">Wert</span><span class="sxs-lookup"><span data-stu-id="9a969-177">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9a969-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a969-178">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9a969-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a969-179">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9a969-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a969-180">System-Only</span></span>            | <span data-ttu-id="9a969-181">False</span><span class="sxs-lookup"><span data-stu-id="9a969-181">False</span></span>                                                          |
| <span data-ttu-id="9a969-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a969-182">Is-Single-Valued</span></span>       | <span data-ttu-id="9a969-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a969-183">True</span></span>                                                           |
| <span data-ttu-id="9a969-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a969-184">Is Indexed</span></span>             | <span data-ttu-id="9a969-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a969-185">True</span></span>                                                           |
| <span data-ttu-id="9a969-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a969-186">In Global Catalog</span></span>      | <span data-ttu-id="9a969-187">False</span><span class="sxs-lookup"><span data-stu-id="9a969-187">False</span></span>                                                          |
| <span data-ttu-id="9a969-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a969-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a969-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a969-189">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9a969-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a969-190">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="9a969-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a969-191">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="9a969-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a969-192">Search-Flags</span></span>           | <span data-ttu-id="9a969-193">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9a969-193">0x00000001</span></span>                                                     |
| <span data-ttu-id="9a969-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a969-194">System-Flags</span></span>           | <span data-ttu-id="9a969-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a969-195">0x00000000</span></span>                                                     |
| <span data-ttu-id="9a969-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a969-196">Classes used in</span></span>        | [<span data-ttu-id="9a969-197">**msSFU-30-Domäne-Info**</span><span class="sxs-lookup"><span data-stu-id="9a969-197">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9a969-198">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9a969-198">Windows Server 2012</span></span>



| <span data-ttu-id="9a969-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a969-199">Entry</span></span> | <span data-ttu-id="9a969-200">Wert</span><span class="sxs-lookup"><span data-stu-id="9a969-200">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9a969-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="9a969-201">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9a969-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9a969-202">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="9a969-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="9a969-203">System-Only</span></span>            | <span data-ttu-id="9a969-204">False</span><span class="sxs-lookup"><span data-stu-id="9a969-204">False</span></span>                                                          |
| <span data-ttu-id="9a969-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="9a969-205">Is-Single-Valued</span></span>       | <span data-ttu-id="9a969-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a969-206">True</span></span>                                                           |
| <span data-ttu-id="9a969-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="9a969-207">Is Indexed</span></span>             | <span data-ttu-id="9a969-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="9a969-208">True</span></span>                                                           |
| <span data-ttu-id="9a969-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="9a969-209">In Global Catalog</span></span>      | <span data-ttu-id="9a969-210">False</span><span class="sxs-lookup"><span data-stu-id="9a969-210">False</span></span>                                                          |
| <span data-ttu-id="9a969-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9a969-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="9a969-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="9a969-212">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="9a969-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9a969-213">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="9a969-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9a969-214">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="9a969-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9a969-215">Search-Flags</span></span>           | <span data-ttu-id="9a969-216">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9a969-216">0x00000001</span></span>                                                     |
| <span data-ttu-id="9a969-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9a969-217">System-Flags</span></span>           | <span data-ttu-id="9a969-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9a969-218">0x00000000</span></span>                                                     |
| <span data-ttu-id="9a969-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="9a969-219">Classes used in</span></span>        | [<span data-ttu-id="9a969-220">**msSFU-30-Domäne-Info**</span><span class="sxs-lookup"><span data-stu-id="9a969-220">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



 

 





