---
title: Address-Book-Roots-Attribut
description: Wird von Exchange verwendet. Exchange konfiguriert Strukturen von Adressbuch Containern, die im MAPI-Adressbuch angezeigt werden. Dieses Attribut für das Exchange-Konfigurationsobjekt listet die Stämme der Adressbuch Container-Strukturen auf. | Address-Book-Roots-Attribut
ms.assetid: 7e6d2677-9818-4870-8429-50f73f9c8c1f
ms.tgt_platform: multiple
keywords:
- AD-Schema des Address-Book-Roots-Attributs
- AD-Schema des addressBookRoots-Attributs
topic_type:
- apiref
api_name:
- Address-Book-Roots
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab195744bb7fb5029a9a48aeca55d703e6e05b62
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106357179"
---
# <a name="address-book-roots-attribute"></a><span data-ttu-id="238f9-108">Address-Book-Roots-Attribut</span><span class="sxs-lookup"><span data-stu-id="238f9-108">Address-Book-Roots attribute</span></span>

<span data-ttu-id="238f9-109">Wird von Exchange verwendet.</span><span class="sxs-lookup"><span data-stu-id="238f9-109">Used by Exchange.</span></span> <span data-ttu-id="238f9-110">Exchange konfiguriert Strukturen von Adressbuch Containern, die im MAPI-Adressbuch angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="238f9-110">Exchange configures trees of address book containers to show up in the MAPI address book.</span></span> <span data-ttu-id="238f9-111">Dieses Attribut für das Exchange-Konfigurationsobjekt listet die Stämme der Adressbuch Container-Strukturen auf.</span><span class="sxs-lookup"><span data-stu-id="238f9-111">This attribute on the Exchange Config object lists the roots of the address book container trees.</span></span>



| <span data-ttu-id="238f9-112">Eingabe</span><span class="sxs-lookup"><span data-stu-id="238f9-112">Entry</span></span> | <span data-ttu-id="238f9-113">Wert</span><span class="sxs-lookup"><span data-stu-id="238f9-113">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="238f9-114">CN</span><span class="sxs-lookup"><span data-stu-id="238f9-114">CN</span></span>                | <span data-ttu-id="238f9-115">Address-Book-Stämme</span><span class="sxs-lookup"><span data-stu-id="238f9-115">Address-Book-Roots</span></span>                      |
| <span data-ttu-id="238f9-116">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="238f9-116">Ldap-Display-Name</span></span> | <span data-ttu-id="238f9-117">addressBookRoots</span><span class="sxs-lookup"><span data-stu-id="238f9-117">addressBookRoots</span></span>                        |
| <span data-ttu-id="238f9-118">Size</span><span class="sxs-lookup"><span data-stu-id="238f9-118">Size</span></span>              | \-                                      |
| <span data-ttu-id="238f9-119">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="238f9-119">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="238f9-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="238f9-120">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="238f9-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="238f9-121">Attribute-Id</span></span>      | <span data-ttu-id="238f9-122">1.2.840.113556.1.4.1244</span><span class="sxs-lookup"><span data-stu-id="238f9-122">1.2.840.113556.1.4.1244</span></span>                 |
| <span data-ttu-id="238f9-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="238f9-123">System-Id-Guid</span></span>    | <span data-ttu-id="238f9-124">f70b6e48-06f4-11d2-aa53-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="238f9-124">f70b6e48-06f4-11d2-aa53-00c04fd7d83a</span></span>    |
| <span data-ttu-id="238f9-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="238f9-125">Syntax</span></span>            | [<span data-ttu-id="238f9-126">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="238f9-126">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="238f9-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="238f9-127">Implementations</span></span>

-   [<span data-ttu-id="238f9-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="238f9-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="238f9-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="238f9-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="238f9-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="238f9-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="238f9-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="238f9-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="238f9-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="238f9-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="238f9-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="238f9-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="238f9-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="238f9-134">Windows 2000 Server</span></span>



| <span data-ttu-id="238f9-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="238f9-135">Entry</span></span> | <span data-ttu-id="238f9-136">Wert</span><span class="sxs-lookup"><span data-stu-id="238f9-136">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="238f9-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="238f9-137">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="238f9-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="238f9-138">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="238f9-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="238f9-139">System-Only</span></span>            | <span data-ttu-id="238f9-140">False</span><span class="sxs-lookup"><span data-stu-id="238f9-140">False</span></span>                                                                                |
| <span data-ttu-id="238f9-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="238f9-141">Is-Single-Valued</span></span>       | <span data-ttu-id="238f9-142">False</span><span class="sxs-lookup"><span data-stu-id="238f9-142">False</span></span>                                                                                |
| <span data-ttu-id="238f9-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="238f9-143">Is Indexed</span></span>             | <span data-ttu-id="238f9-144">False</span><span class="sxs-lookup"><span data-stu-id="238f9-144">False</span></span>                                                                                |
| <span data-ttu-id="238f9-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="238f9-145">In Global Catalog</span></span>      | <span data-ttu-id="238f9-146">False</span><span class="sxs-lookup"><span data-stu-id="238f9-146">False</span></span>                                                                                |
| <span data-ttu-id="238f9-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="238f9-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="238f9-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="238f9-148">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="238f9-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="238f9-149">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="238f9-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="238f9-150">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="238f9-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="238f9-151">Search-Flags</span></span>           | <span data-ttu-id="238f9-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="238f9-152">0x00000000</span></span>                                                                           |
| <span data-ttu-id="238f9-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="238f9-153">System-Flags</span></span>           | <span data-ttu-id="238f9-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="238f9-154">0x00000010</span></span>                                                                           |
| <span data-ttu-id="238f9-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="238f9-155">Classes used in</span></span>        | [<span data-ttu-id="238f9-156">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="238f9-156">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="238f9-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="238f9-157">Windows Server 2003</span></span>



| <span data-ttu-id="238f9-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="238f9-158">Entry</span></span> | <span data-ttu-id="238f9-159">Wert</span><span class="sxs-lookup"><span data-stu-id="238f9-159">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="238f9-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="238f9-160">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="238f9-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="238f9-161">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="238f9-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="238f9-162">System-Only</span></span>            | <span data-ttu-id="238f9-163">False</span><span class="sxs-lookup"><span data-stu-id="238f9-163">False</span></span>                                                                                |
| <span data-ttu-id="238f9-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="238f9-164">Is-Single-Valued</span></span>       | <span data-ttu-id="238f9-165">False</span><span class="sxs-lookup"><span data-stu-id="238f9-165">False</span></span>                                                                                |
| <span data-ttu-id="238f9-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="238f9-166">Is Indexed</span></span>             | <span data-ttu-id="238f9-167">False</span><span class="sxs-lookup"><span data-stu-id="238f9-167">False</span></span>                                                                                |
| <span data-ttu-id="238f9-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="238f9-168">In Global Catalog</span></span>      | <span data-ttu-id="238f9-169">False</span><span class="sxs-lookup"><span data-stu-id="238f9-169">False</span></span>                                                                                |
| <span data-ttu-id="238f9-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="238f9-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="238f9-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="238f9-171">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="238f9-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="238f9-172">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="238f9-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="238f9-173">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="238f9-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="238f9-174">Search-Flags</span></span>           | <span data-ttu-id="238f9-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="238f9-175">0x00000000</span></span>                                                                           |
| <span data-ttu-id="238f9-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="238f9-176">System-Flags</span></span>           | <span data-ttu-id="238f9-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="238f9-177">0x00000010</span></span>                                                                           |
| <span data-ttu-id="238f9-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="238f9-178">Classes used in</span></span>        | [<span data-ttu-id="238f9-179">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="238f9-179">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="238f9-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="238f9-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="238f9-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="238f9-181">Entry</span></span> | <span data-ttu-id="238f9-182">Wert</span><span class="sxs-lookup"><span data-stu-id="238f9-182">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="238f9-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="238f9-183">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="238f9-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="238f9-184">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="238f9-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="238f9-185">System-Only</span></span>            | <span data-ttu-id="238f9-186">False</span><span class="sxs-lookup"><span data-stu-id="238f9-186">False</span></span>                                                                                |
| <span data-ttu-id="238f9-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="238f9-187">Is-Single-Valued</span></span>       | <span data-ttu-id="238f9-188">False</span><span class="sxs-lookup"><span data-stu-id="238f9-188">False</span></span>                                                                                |
| <span data-ttu-id="238f9-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="238f9-189">Is Indexed</span></span>             | <span data-ttu-id="238f9-190">False</span><span class="sxs-lookup"><span data-stu-id="238f9-190">False</span></span>                                                                                |
| <span data-ttu-id="238f9-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="238f9-191">In Global Catalog</span></span>      | <span data-ttu-id="238f9-192">False</span><span class="sxs-lookup"><span data-stu-id="238f9-192">False</span></span>                                                                                |
| <span data-ttu-id="238f9-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="238f9-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="238f9-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="238f9-194">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="238f9-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="238f9-195">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="238f9-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="238f9-196">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="238f9-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="238f9-197">Search-Flags</span></span>           | <span data-ttu-id="238f9-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="238f9-198">0x00000000</span></span>                                                                           |
| <span data-ttu-id="238f9-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="238f9-199">System-Flags</span></span>           | <span data-ttu-id="238f9-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="238f9-200">0x00000010</span></span>                                                                           |
| <span data-ttu-id="238f9-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="238f9-201">Classes used in</span></span>        | [<span data-ttu-id="238f9-202">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="238f9-202">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="238f9-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="238f9-203">Windows Server 2008</span></span>



| <span data-ttu-id="238f9-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="238f9-204">Entry</span></span> | <span data-ttu-id="238f9-205">Wert</span><span class="sxs-lookup"><span data-stu-id="238f9-205">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="238f9-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="238f9-206">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="238f9-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="238f9-207">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="238f9-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="238f9-208">System-Only</span></span>            | <span data-ttu-id="238f9-209">False</span><span class="sxs-lookup"><span data-stu-id="238f9-209">False</span></span>                                                                                |
| <span data-ttu-id="238f9-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="238f9-210">Is-Single-Valued</span></span>       | <span data-ttu-id="238f9-211">False</span><span class="sxs-lookup"><span data-stu-id="238f9-211">False</span></span>                                                                                |
| <span data-ttu-id="238f9-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="238f9-212">Is Indexed</span></span>             | <span data-ttu-id="238f9-213">False</span><span class="sxs-lookup"><span data-stu-id="238f9-213">False</span></span>                                                                                |
| <span data-ttu-id="238f9-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="238f9-214">In Global Catalog</span></span>      | <span data-ttu-id="238f9-215">False</span><span class="sxs-lookup"><span data-stu-id="238f9-215">False</span></span>                                                                                |
| <span data-ttu-id="238f9-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="238f9-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="238f9-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="238f9-217">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="238f9-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="238f9-218">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="238f9-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="238f9-219">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="238f9-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="238f9-220">Search-Flags</span></span>           | <span data-ttu-id="238f9-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="238f9-221">0x00000000</span></span>                                                                           |
| <span data-ttu-id="238f9-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="238f9-222">System-Flags</span></span>           | <span data-ttu-id="238f9-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="238f9-223">0x00000010</span></span>                                                                           |
| <span data-ttu-id="238f9-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="238f9-224">Classes used in</span></span>        | [<span data-ttu-id="238f9-225">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="238f9-225">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="238f9-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="238f9-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="238f9-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="238f9-227">Entry</span></span> | <span data-ttu-id="238f9-228">Wert</span><span class="sxs-lookup"><span data-stu-id="238f9-228">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="238f9-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="238f9-229">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="238f9-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="238f9-230">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="238f9-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="238f9-231">System-Only</span></span>            | <span data-ttu-id="238f9-232">False</span><span class="sxs-lookup"><span data-stu-id="238f9-232">False</span></span>                                                                                |
| <span data-ttu-id="238f9-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="238f9-233">Is-Single-Valued</span></span>       | <span data-ttu-id="238f9-234">False</span><span class="sxs-lookup"><span data-stu-id="238f9-234">False</span></span>                                                                                |
| <span data-ttu-id="238f9-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="238f9-235">Is Indexed</span></span>             | <span data-ttu-id="238f9-236">False</span><span class="sxs-lookup"><span data-stu-id="238f9-236">False</span></span>                                                                                |
| <span data-ttu-id="238f9-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="238f9-237">In Global Catalog</span></span>      | <span data-ttu-id="238f9-238">False</span><span class="sxs-lookup"><span data-stu-id="238f9-238">False</span></span>                                                                                |
| <span data-ttu-id="238f9-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="238f9-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="238f9-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="238f9-240">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="238f9-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="238f9-241">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="238f9-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="238f9-242">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="238f9-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="238f9-243">Search-Flags</span></span>           | <span data-ttu-id="238f9-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="238f9-244">0x00000000</span></span>                                                                           |
| <span data-ttu-id="238f9-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="238f9-245">System-Flags</span></span>           | <span data-ttu-id="238f9-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="238f9-246">0x00000010</span></span>                                                                           |
| <span data-ttu-id="238f9-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="238f9-247">Classes used in</span></span>        | [<span data-ttu-id="238f9-248">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="238f9-248">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="238f9-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="238f9-249">Windows Server 2012</span></span>



| <span data-ttu-id="238f9-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="238f9-250">Entry</span></span> | <span data-ttu-id="238f9-251">Wert</span><span class="sxs-lookup"><span data-stu-id="238f9-251">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="238f9-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="238f9-252">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="238f9-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="238f9-253">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="238f9-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="238f9-254">System-Only</span></span>            | <span data-ttu-id="238f9-255">False</span><span class="sxs-lookup"><span data-stu-id="238f9-255">False</span></span>                                                                                |
| <span data-ttu-id="238f9-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="238f9-256">Is-Single-Valued</span></span>       | <span data-ttu-id="238f9-257">False</span><span class="sxs-lookup"><span data-stu-id="238f9-257">False</span></span>                                                                                |
| <span data-ttu-id="238f9-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="238f9-258">Is Indexed</span></span>             | <span data-ttu-id="238f9-259">False</span><span class="sxs-lookup"><span data-stu-id="238f9-259">False</span></span>                                                                                |
| <span data-ttu-id="238f9-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="238f9-260">In Global Catalog</span></span>      | <span data-ttu-id="238f9-261">False</span><span class="sxs-lookup"><span data-stu-id="238f9-261">False</span></span>                                                                                |
| <span data-ttu-id="238f9-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="238f9-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="238f9-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="238f9-263">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="238f9-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="238f9-264">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="238f9-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="238f9-265">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="238f9-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="238f9-266">Search-Flags</span></span>           | <span data-ttu-id="238f9-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="238f9-267">0x00000000</span></span>                                                                           |
| <span data-ttu-id="238f9-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="238f9-268">System-Flags</span></span>           | <span data-ttu-id="238f9-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="238f9-269">0x00000010</span></span>                                                                           |
| <span data-ttu-id="238f9-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="238f9-270">Classes used in</span></span>        | [<span data-ttu-id="238f9-271">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="238f9-271">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





