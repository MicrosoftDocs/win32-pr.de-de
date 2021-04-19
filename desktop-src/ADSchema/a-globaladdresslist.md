---
title: Global-Address-List-Attribut
description: Dieses Attribut wird in einem Microsoft Exchange-Container verwendet, um den Distinguished Name einer neu erstellten globalen Adressliste (GAL) zu speichern.
ms.assetid: 0da2bafe-ecdf-4b75-9461-08a35151b85c
ms.tgt_platform: multiple
keywords:
- AD-Schema des Global-Address-List-Attributs
- Global AddressList-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Global-Address-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28178dfd6621593ee60e6e07043be544445cb6e7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106343077"
---
# <a name="global-address-list-attribute"></a><span data-ttu-id="b297a-105">Global-Address-List-Attribut</span><span class="sxs-lookup"><span data-stu-id="b297a-105">Global-Address-List attribute</span></span>

<span data-ttu-id="b297a-106">Dieses Attribut wird in einem Microsoft Exchange-Container verwendet, um den Distinguished Name einer neu erstellten globalen Adressliste (GAL) zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b297a-106">This attribute is used on a Microsoft Exchange container to store the distinguished name of a newly created global address list (GAL).</span></span> <span data-ttu-id="b297a-107">Dieses Attribut muss über einen Eintrag verfügen, bevor Sie Messaging Application Programming Interface (MAPI)-Clients für die Verwendung eines GAL aktivieren können.</span><span class="sxs-lookup"><span data-stu-id="b297a-107">This attribute must have an entry before you can enable Messaging Application Programming Interface (MAPI) clients to use a GAL.</span></span>



| <span data-ttu-id="b297a-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b297a-108">Entry</span></span> | <span data-ttu-id="b297a-109">Wert</span><span class="sxs-lookup"><span data-stu-id="b297a-109">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="b297a-110">CN</span><span class="sxs-lookup"><span data-stu-id="b297a-110">CN</span></span>                | <span data-ttu-id="b297a-111">Global-Address-List</span><span class="sxs-lookup"><span data-stu-id="b297a-111">Global-Address-List</span></span>                     |
| <span data-ttu-id="b297a-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b297a-112">Ldap-Display-Name</span></span> | <span data-ttu-id="b297a-113">GlobalAddressList</span><span class="sxs-lookup"><span data-stu-id="b297a-113">globalAddressList</span></span>                       |
| <span data-ttu-id="b297a-114">Size</span><span class="sxs-lookup"><span data-stu-id="b297a-114">Size</span></span>              | \-                                      |
| <span data-ttu-id="b297a-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b297a-115">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="b297a-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="b297a-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="b297a-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b297a-117">Attribute-Id</span></span>      | <span data-ttu-id="b297a-118">1.2.840.113556.1.4.1245</span><span class="sxs-lookup"><span data-stu-id="b297a-118">1.2.840.113556.1.4.1245</span></span>                 |
| <span data-ttu-id="b297a-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b297a-119">System-Id-Guid</span></span>    | <span data-ttu-id="b297a-120">f754c748-06f4-11d2-aa53-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="b297a-120">f754c748-06f4-11d2-aa53-00c04fd7d83a</span></span>    |
| <span data-ttu-id="b297a-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="b297a-121">Syntax</span></span>            | [<span data-ttu-id="b297a-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="b297a-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="b297a-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="b297a-123">Implementations</span></span>

-   [<span data-ttu-id="b297a-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b297a-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b297a-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b297a-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b297a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b297a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b297a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b297a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b297a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b297a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b297a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b297a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b297a-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b297a-130">Windows 2000 Server</span></span>



| <span data-ttu-id="b297a-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b297a-131">Entry</span></span> | <span data-ttu-id="b297a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b297a-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b297a-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b297a-133">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="b297a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b297a-134">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="b297a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b297a-135">System-Only</span></span>            | <span data-ttu-id="b297a-136">False</span><span class="sxs-lookup"><span data-stu-id="b297a-136">False</span></span>                                                                                |
| <span data-ttu-id="b297a-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b297a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b297a-138">False</span><span class="sxs-lookup"><span data-stu-id="b297a-138">False</span></span>                                                                                |
| <span data-ttu-id="b297a-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b297a-139">Is Indexed</span></span>             | <span data-ttu-id="b297a-140">False</span><span class="sxs-lookup"><span data-stu-id="b297a-140">False</span></span>                                                                                |
| <span data-ttu-id="b297a-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b297a-141">In Global Catalog</span></span>      | <span data-ttu-id="b297a-142">False</span><span class="sxs-lookup"><span data-stu-id="b297a-142">False</span></span>                                                                                |
| <span data-ttu-id="b297a-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b297a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b297a-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b297a-144">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="b297a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b297a-145">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="b297a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b297a-146">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="b297a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b297a-147">Search-Flags</span></span>           | <span data-ttu-id="b297a-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b297a-148">0x00000000</span></span>                                                                           |
| <span data-ttu-id="b297a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b297a-149">System-Flags</span></span>           | <span data-ttu-id="b297a-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b297a-150">0x00000010</span></span>                                                                           |
| <span data-ttu-id="b297a-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b297a-151">Classes used in</span></span>        | [<span data-ttu-id="b297a-152">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="b297a-152">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b297a-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b297a-153">Windows Server 2003</span></span>



| <span data-ttu-id="b297a-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b297a-154">Entry</span></span> | <span data-ttu-id="b297a-155">Wert</span><span class="sxs-lookup"><span data-stu-id="b297a-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b297a-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b297a-156">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="b297a-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b297a-157">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="b297a-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="b297a-158">System-Only</span></span>            | <span data-ttu-id="b297a-159">False</span><span class="sxs-lookup"><span data-stu-id="b297a-159">False</span></span>                                                                                |
| <span data-ttu-id="b297a-160">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b297a-160">Is-Single-Valued</span></span>       | <span data-ttu-id="b297a-161">False</span><span class="sxs-lookup"><span data-stu-id="b297a-161">False</span></span>                                                                                |
| <span data-ttu-id="b297a-162">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b297a-162">Is Indexed</span></span>             | <span data-ttu-id="b297a-163">False</span><span class="sxs-lookup"><span data-stu-id="b297a-163">False</span></span>                                                                                |
| <span data-ttu-id="b297a-164">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b297a-164">In Global Catalog</span></span>      | <span data-ttu-id="b297a-165">False</span><span class="sxs-lookup"><span data-stu-id="b297a-165">False</span></span>                                                                                |
| <span data-ttu-id="b297a-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b297a-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="b297a-167">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b297a-167">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="b297a-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b297a-168">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="b297a-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b297a-169">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="b297a-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b297a-170">Search-Flags</span></span>           | <span data-ttu-id="b297a-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b297a-171">0x00000000</span></span>                                                                           |
| <span data-ttu-id="b297a-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b297a-172">System-Flags</span></span>           | <span data-ttu-id="b297a-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b297a-173">0x00000010</span></span>                                                                           |
| <span data-ttu-id="b297a-174">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b297a-174">Classes used in</span></span>        | [<span data-ttu-id="b297a-175">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="b297a-175">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b297a-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b297a-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b297a-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b297a-177">Entry</span></span> | <span data-ttu-id="b297a-178">Wert</span><span class="sxs-lookup"><span data-stu-id="b297a-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b297a-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b297a-179">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="b297a-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b297a-180">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="b297a-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b297a-181">System-Only</span></span>            | <span data-ttu-id="b297a-182">False</span><span class="sxs-lookup"><span data-stu-id="b297a-182">False</span></span>                                                                                |
| <span data-ttu-id="b297a-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b297a-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b297a-184">False</span><span class="sxs-lookup"><span data-stu-id="b297a-184">False</span></span>                                                                                |
| <span data-ttu-id="b297a-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b297a-185">Is Indexed</span></span>             | <span data-ttu-id="b297a-186">False</span><span class="sxs-lookup"><span data-stu-id="b297a-186">False</span></span>                                                                                |
| <span data-ttu-id="b297a-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b297a-187">In Global Catalog</span></span>      | <span data-ttu-id="b297a-188">False</span><span class="sxs-lookup"><span data-stu-id="b297a-188">False</span></span>                                                                                |
| <span data-ttu-id="b297a-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b297a-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b297a-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b297a-190">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="b297a-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b297a-191">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="b297a-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b297a-192">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="b297a-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b297a-193">Search-Flags</span></span>           | <span data-ttu-id="b297a-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b297a-194">0x00000000</span></span>                                                                           |
| <span data-ttu-id="b297a-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b297a-195">System-Flags</span></span>           | <span data-ttu-id="b297a-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b297a-196">0x00000010</span></span>                                                                           |
| <span data-ttu-id="b297a-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b297a-197">Classes used in</span></span>        | [<span data-ttu-id="b297a-198">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="b297a-198">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b297a-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b297a-199">Windows Server 2008</span></span>



| <span data-ttu-id="b297a-200">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b297a-200">Entry</span></span> | <span data-ttu-id="b297a-201">Wert</span><span class="sxs-lookup"><span data-stu-id="b297a-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b297a-202">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b297a-202">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="b297a-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b297a-203">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="b297a-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="b297a-204">System-Only</span></span>            | <span data-ttu-id="b297a-205">False</span><span class="sxs-lookup"><span data-stu-id="b297a-205">False</span></span>                                                                                |
| <span data-ttu-id="b297a-206">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b297a-206">Is-Single-Valued</span></span>       | <span data-ttu-id="b297a-207">False</span><span class="sxs-lookup"><span data-stu-id="b297a-207">False</span></span>                                                                                |
| <span data-ttu-id="b297a-208">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b297a-208">Is Indexed</span></span>             | <span data-ttu-id="b297a-209">False</span><span class="sxs-lookup"><span data-stu-id="b297a-209">False</span></span>                                                                                |
| <span data-ttu-id="b297a-210">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b297a-210">In Global Catalog</span></span>      | <span data-ttu-id="b297a-211">False</span><span class="sxs-lookup"><span data-stu-id="b297a-211">False</span></span>                                                                                |
| <span data-ttu-id="b297a-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b297a-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="b297a-213">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b297a-213">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="b297a-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b297a-214">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="b297a-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b297a-215">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="b297a-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b297a-216">Search-Flags</span></span>           | <span data-ttu-id="b297a-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b297a-217">0x00000000</span></span>                                                                           |
| <span data-ttu-id="b297a-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b297a-218">System-Flags</span></span>           | <span data-ttu-id="b297a-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b297a-219">0x00000010</span></span>                                                                           |
| <span data-ttu-id="b297a-220">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b297a-220">Classes used in</span></span>        | [<span data-ttu-id="b297a-221">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="b297a-221">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b297a-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b297a-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b297a-223">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b297a-223">Entry</span></span> | <span data-ttu-id="b297a-224">Wert</span><span class="sxs-lookup"><span data-stu-id="b297a-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b297a-225">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b297a-225">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="b297a-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b297a-226">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="b297a-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b297a-227">System-Only</span></span>            | <span data-ttu-id="b297a-228">False</span><span class="sxs-lookup"><span data-stu-id="b297a-228">False</span></span>                                                                                |
| <span data-ttu-id="b297a-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b297a-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b297a-230">False</span><span class="sxs-lookup"><span data-stu-id="b297a-230">False</span></span>                                                                                |
| <span data-ttu-id="b297a-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b297a-231">Is Indexed</span></span>             | <span data-ttu-id="b297a-232">False</span><span class="sxs-lookup"><span data-stu-id="b297a-232">False</span></span>                                                                                |
| <span data-ttu-id="b297a-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b297a-233">In Global Catalog</span></span>      | <span data-ttu-id="b297a-234">False</span><span class="sxs-lookup"><span data-stu-id="b297a-234">False</span></span>                                                                                |
| <span data-ttu-id="b297a-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b297a-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b297a-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b297a-236">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="b297a-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b297a-237">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="b297a-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b297a-238">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="b297a-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b297a-239">Search-Flags</span></span>           | <span data-ttu-id="b297a-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b297a-240">0x00000000</span></span>                                                                           |
| <span data-ttu-id="b297a-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b297a-241">System-Flags</span></span>           | <span data-ttu-id="b297a-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b297a-242">0x00000010</span></span>                                                                           |
| <span data-ttu-id="b297a-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b297a-243">Classes used in</span></span>        | [<span data-ttu-id="b297a-244">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="b297a-244">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b297a-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b297a-245">Windows Server 2012</span></span>



| <span data-ttu-id="b297a-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b297a-246">Entry</span></span> | <span data-ttu-id="b297a-247">Wert</span><span class="sxs-lookup"><span data-stu-id="b297a-247">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b297a-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="b297a-248">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="b297a-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b297a-249">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="b297a-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="b297a-250">System-Only</span></span>            | <span data-ttu-id="b297a-251">False</span><span class="sxs-lookup"><span data-stu-id="b297a-251">False</span></span>                                                                                |
| <span data-ttu-id="b297a-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="b297a-252">Is-Single-Valued</span></span>       | <span data-ttu-id="b297a-253">False</span><span class="sxs-lookup"><span data-stu-id="b297a-253">False</span></span>                                                                                |
| <span data-ttu-id="b297a-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="b297a-254">Is Indexed</span></span>             | <span data-ttu-id="b297a-255">False</span><span class="sxs-lookup"><span data-stu-id="b297a-255">False</span></span>                                                                                |
| <span data-ttu-id="b297a-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="b297a-256">In Global Catalog</span></span>      | <span data-ttu-id="b297a-257">False</span><span class="sxs-lookup"><span data-stu-id="b297a-257">False</span></span>                                                                                |
| <span data-ttu-id="b297a-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b297a-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="b297a-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="b297a-259">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="b297a-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b297a-260">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="b297a-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b297a-261">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="b297a-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b297a-262">Search-Flags</span></span>           | <span data-ttu-id="b297a-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b297a-263">0x00000000</span></span>                                                                           |
| <span data-ttu-id="b297a-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b297a-264">System-Flags</span></span>           | <span data-ttu-id="b297a-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b297a-265">0x00000010</span></span>                                                                           |
| <span data-ttu-id="b297a-266">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="b297a-266">Classes used in</span></span>        | [<span data-ttu-id="b297a-267">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="b297a-267">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





