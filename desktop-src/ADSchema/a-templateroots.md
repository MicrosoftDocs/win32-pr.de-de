---
title: Template-Roots-Attribut
description: Dieses Attribut wird im Exchange-Konfigurations Container verwendet, um anzugeben, wo die Vorlagen Container gespeichert werden. Diese Informationen werden vom Active Directory MAPI-Anbieter verwendet.
ms.assetid: 1416ce4a-ca07-4ca9-8ea1-e1a6ad19e7ad
ms.tgt_platform: multiple
keywords:
- AD-Schema für Template-Roots-Attribut
- templateroots-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Template-Roots
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 761c6d3d79bbf45e9a4d391b612956d6893cd314
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744897"
---
# <a name="template-roots-attribute"></a><span data-ttu-id="cc2de-106">Template-Roots-Attribut</span><span class="sxs-lookup"><span data-stu-id="cc2de-106">Template-Roots attribute</span></span>

<span data-ttu-id="cc2de-107">Dieses Attribut wird im Exchange-Konfigurations Container verwendet, um anzugeben, wo die Vorlagen Container gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="cc2de-107">This attribute is used on the Exchange config container to indicate where the template containers are stored.</span></span> <span data-ttu-id="cc2de-108">Diese Informationen werden vom Active Directory MAPI-Anbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc2de-108">This information is used by the Active Directory MAPI provider.</span></span>



| <span data-ttu-id="cc2de-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cc2de-109">Entry</span></span> | <span data-ttu-id="cc2de-110">Wert</span><span class="sxs-lookup"><span data-stu-id="cc2de-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="cc2de-111">CN</span><span class="sxs-lookup"><span data-stu-id="cc2de-111">CN</span></span>                | <span data-ttu-id="cc2de-112">Template-Roots</span><span class="sxs-lookup"><span data-stu-id="cc2de-112">Template-Roots</span></span>                          |
| <span data-ttu-id="cc2de-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cc2de-113">Ldap-Display-Name</span></span> | <span data-ttu-id="cc2de-114">templateroots</span><span class="sxs-lookup"><span data-stu-id="cc2de-114">templateRoots</span></span>                           |
| <span data-ttu-id="cc2de-115">Size</span><span class="sxs-lookup"><span data-stu-id="cc2de-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="cc2de-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="cc2de-116">Update Privilege</span></span>  | <span data-ttu-id="cc2de-117">Diese wird vom System verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc2de-117">This is used by the system.</span></span>             |
| <span data-ttu-id="cc2de-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="cc2de-118">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="cc2de-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cc2de-119">Attribute-Id</span></span>      | <span data-ttu-id="cc2de-120">1.2.840.113556.1.4.1346</span><span class="sxs-lookup"><span data-stu-id="cc2de-120">1.2.840.113556.1.4.1346</span></span>                 |
| <span data-ttu-id="cc2de-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cc2de-121">System-Id-Guid</span></span>    | <span data-ttu-id="cc2de-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="cc2de-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span></span>    |
| <span data-ttu-id="cc2de-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc2de-123">Syntax</span></span>            | [<span data-ttu-id="cc2de-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="cc2de-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="cc2de-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="cc2de-125">Implementations</span></span>

-   [<span data-ttu-id="cc2de-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cc2de-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cc2de-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cc2de-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cc2de-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cc2de-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cc2de-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cc2de-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cc2de-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cc2de-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cc2de-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cc2de-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cc2de-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cc2de-132">Windows 2000 Server</span></span>



| <span data-ttu-id="cc2de-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cc2de-133">Entry</span></span> | <span data-ttu-id="cc2de-134">Wert</span><span class="sxs-lookup"><span data-stu-id="cc2de-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc2de-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cc2de-135">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="cc2de-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc2de-136">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="cc2de-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc2de-137">System-Only</span></span>            | <span data-ttu-id="cc2de-138">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-138">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cc2de-139">Is-Single-Valued</span></span>       | <span data-ttu-id="cc2de-140">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-140">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cc2de-141">Is Indexed</span></span>             | <span data-ttu-id="cc2de-142">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-142">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cc2de-143">In Global Catalog</span></span>      | <span data-ttu-id="cc2de-144">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-144">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cc2de-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc2de-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cc2de-146">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="cc2de-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc2de-147">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="cc2de-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc2de-148">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="cc2de-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc2de-149">Search-Flags</span></span>           | <span data-ttu-id="cc2de-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc2de-150">0x00000000</span></span>                                                                           |
| <span data-ttu-id="cc2de-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc2de-151">System-Flags</span></span>           | <span data-ttu-id="cc2de-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc2de-152">0x00000010</span></span>                                                                           |
| <span data-ttu-id="cc2de-153">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cc2de-153">Classes used in</span></span>        | [<span data-ttu-id="cc2de-154">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="cc2de-154">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cc2de-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cc2de-155">Windows Server 2003</span></span>



| <span data-ttu-id="cc2de-156">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cc2de-156">Entry</span></span> | <span data-ttu-id="cc2de-157">Wert</span><span class="sxs-lookup"><span data-stu-id="cc2de-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc2de-158">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cc2de-158">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="cc2de-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc2de-159">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="cc2de-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc2de-160">System-Only</span></span>            | <span data-ttu-id="cc2de-161">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-161">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-162">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cc2de-162">Is-Single-Valued</span></span>       | <span data-ttu-id="cc2de-163">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-163">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-164">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cc2de-164">Is Indexed</span></span>             | <span data-ttu-id="cc2de-165">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-165">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-166">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cc2de-166">In Global Catalog</span></span>      | <span data-ttu-id="cc2de-167">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-167">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cc2de-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc2de-169">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cc2de-169">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="cc2de-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc2de-170">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="cc2de-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc2de-171">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="cc2de-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc2de-172">Search-Flags</span></span>           | <span data-ttu-id="cc2de-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc2de-173">0x00000000</span></span>                                                                           |
| <span data-ttu-id="cc2de-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc2de-174">System-Flags</span></span>           | <span data-ttu-id="cc2de-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc2de-175">0x00000010</span></span>                                                                           |
| <span data-ttu-id="cc2de-176">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cc2de-176">Classes used in</span></span>        | [<span data-ttu-id="cc2de-177">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="cc2de-177">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cc2de-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cc2de-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cc2de-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cc2de-179">Entry</span></span> | <span data-ttu-id="cc2de-180">Wert</span><span class="sxs-lookup"><span data-stu-id="cc2de-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc2de-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cc2de-181">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="cc2de-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc2de-182">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="cc2de-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc2de-183">System-Only</span></span>            | <span data-ttu-id="cc2de-184">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-184">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cc2de-185">Is-Single-Valued</span></span>       | <span data-ttu-id="cc2de-186">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-186">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cc2de-187">Is Indexed</span></span>             | <span data-ttu-id="cc2de-188">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-188">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cc2de-189">In Global Catalog</span></span>      | <span data-ttu-id="cc2de-190">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-190">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cc2de-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc2de-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cc2de-192">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="cc2de-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc2de-193">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="cc2de-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc2de-194">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="cc2de-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc2de-195">Search-Flags</span></span>           | <span data-ttu-id="cc2de-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc2de-196">0x00000000</span></span>                                                                           |
| <span data-ttu-id="cc2de-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc2de-197">System-Flags</span></span>           | <span data-ttu-id="cc2de-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc2de-198">0x00000010</span></span>                                                                           |
| <span data-ttu-id="cc2de-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cc2de-199">Classes used in</span></span>        | [<span data-ttu-id="cc2de-200">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="cc2de-200">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cc2de-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc2de-201">Windows Server 2008</span></span>



| <span data-ttu-id="cc2de-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cc2de-202">Entry</span></span> | <span data-ttu-id="cc2de-203">Wert</span><span class="sxs-lookup"><span data-stu-id="cc2de-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc2de-204">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cc2de-204">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="cc2de-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc2de-205">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="cc2de-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc2de-206">System-Only</span></span>            | <span data-ttu-id="cc2de-207">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-207">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-208">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cc2de-208">Is-Single-Valued</span></span>       | <span data-ttu-id="cc2de-209">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-209">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-210">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cc2de-210">Is Indexed</span></span>             | <span data-ttu-id="cc2de-211">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-211">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-212">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cc2de-212">In Global Catalog</span></span>      | <span data-ttu-id="cc2de-213">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-213">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cc2de-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc2de-215">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cc2de-215">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="cc2de-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc2de-216">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="cc2de-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc2de-217">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="cc2de-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc2de-218">Search-Flags</span></span>           | <span data-ttu-id="cc2de-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc2de-219">0x00000000</span></span>                                                                           |
| <span data-ttu-id="cc2de-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc2de-220">System-Flags</span></span>           | <span data-ttu-id="cc2de-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc2de-221">0x00000010</span></span>                                                                           |
| <span data-ttu-id="cc2de-222">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cc2de-222">Classes used in</span></span>        | [<span data-ttu-id="cc2de-223">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="cc2de-223">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cc2de-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cc2de-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cc2de-225">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cc2de-225">Entry</span></span> | <span data-ttu-id="cc2de-226">Wert</span><span class="sxs-lookup"><span data-stu-id="cc2de-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc2de-227">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cc2de-227">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="cc2de-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc2de-228">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="cc2de-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc2de-229">System-Only</span></span>            | <span data-ttu-id="cc2de-230">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-230">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-231">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cc2de-231">Is-Single-Valued</span></span>       | <span data-ttu-id="cc2de-232">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-232">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-233">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cc2de-233">Is Indexed</span></span>             | <span data-ttu-id="cc2de-234">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-234">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-235">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cc2de-235">In Global Catalog</span></span>      | <span data-ttu-id="cc2de-236">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-236">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cc2de-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc2de-238">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cc2de-238">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="cc2de-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc2de-239">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="cc2de-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc2de-240">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="cc2de-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc2de-241">Search-Flags</span></span>           | <span data-ttu-id="cc2de-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc2de-242">0x00000000</span></span>                                                                           |
| <span data-ttu-id="cc2de-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc2de-243">System-Flags</span></span>           | <span data-ttu-id="cc2de-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc2de-244">0x00000010</span></span>                                                                           |
| <span data-ttu-id="cc2de-245">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cc2de-245">Classes used in</span></span>        | [<span data-ttu-id="cc2de-246">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="cc2de-246">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cc2de-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cc2de-247">Windows Server 2012</span></span>



| <span data-ttu-id="cc2de-248">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cc2de-248">Entry</span></span> | <span data-ttu-id="cc2de-249">Wert</span><span class="sxs-lookup"><span data-stu-id="cc2de-249">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc2de-250">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cc2de-250">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="cc2de-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc2de-251">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="cc2de-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc2de-252">System-Only</span></span>            | <span data-ttu-id="cc2de-253">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-253">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-254">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cc2de-254">Is-Single-Valued</span></span>       | <span data-ttu-id="cc2de-255">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-255">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-256">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cc2de-256">Is Indexed</span></span>             | <span data-ttu-id="cc2de-257">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-257">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-258">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cc2de-258">In Global Catalog</span></span>      | <span data-ttu-id="cc2de-259">False</span><span class="sxs-lookup"><span data-stu-id="cc2de-259">False</span></span>                                                                                |
| <span data-ttu-id="cc2de-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cc2de-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc2de-261">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cc2de-261">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="cc2de-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc2de-262">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="cc2de-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc2de-263">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="cc2de-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc2de-264">Search-Flags</span></span>           | <span data-ttu-id="cc2de-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc2de-265">0x00000000</span></span>                                                                           |
| <span data-ttu-id="cc2de-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc2de-266">System-Flags</span></span>           | <span data-ttu-id="cc2de-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cc2de-267">0x00000010</span></span>                                                                           |
| <span data-ttu-id="cc2de-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cc2de-268">Classes used in</span></span>        | [<span data-ttu-id="cc2de-269">**ms-Exch-Configuration-Container**</span><span class="sxs-lookup"><span data-stu-id="cc2de-269">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





