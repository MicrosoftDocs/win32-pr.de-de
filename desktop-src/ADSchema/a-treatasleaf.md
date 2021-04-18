---
title: Treat-as-Blatt-Attribut
description: Anzeige-Spezifizierer, bei denen dieses Flag auf true festgelegt ist, erzwingen die Anzeige der verknüpften Klasse als Blatt Klasse, auch wenn Sie über untergeordnete Elemente verfügt.
ms.assetid: 7b19fc04-69ac-4e4b-8b9b-bd1ec74fcea7
ms.tgt_platform: multiple
keywords:
- AD-Schema des Treat-as-Blatt-Attributs
- AD-Schema des treatAsLeaf-Attributs
topic_type:
- apiref
api_name:
- Treat-As-Leaf
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60d357fa368818a9b216fe18a394b806e390b46b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106345374"
---
# <a name="treat-as-leaf-attribute"></a><span data-ttu-id="5e07c-105">Treat-as-Blatt-Attribut</span><span class="sxs-lookup"><span data-stu-id="5e07c-105">Treat-As-Leaf attribute</span></span>

<span data-ttu-id="5e07c-106">Anzeige-Spezifizierer, bei denen dieses Flag auf **true** festgelegt ist, erzwingen die Anzeige der verknüpften Klasse als Blatt Klasse, auch wenn Sie über untergeordnete Elemente verfügt.</span><span class="sxs-lookup"><span data-stu-id="5e07c-106">Display-specifiers with this flag set to **TRUE** force the related class to be displayed as a leaf class even if it has children.</span></span>



| <span data-ttu-id="5e07c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5e07c-107">Entry</span></span> | <span data-ttu-id="5e07c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="5e07c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5e07c-109">CN</span><span class="sxs-lookup"><span data-stu-id="5e07c-109">CN</span></span>                | <span data-ttu-id="5e07c-110">Als Blatt behandeln</span><span class="sxs-lookup"><span data-stu-id="5e07c-110">Treat-As-Leaf</span></span>                        |
| <span data-ttu-id="5e07c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5e07c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5e07c-112">behandatenblatt</span><span class="sxs-lookup"><span data-stu-id="5e07c-112">treatAsLeaf</span></span>                          |
| <span data-ttu-id="5e07c-113">Size</span><span class="sxs-lookup"><span data-stu-id="5e07c-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="5e07c-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5e07c-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="5e07c-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="5e07c-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="5e07c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5e07c-116">Attribute-Id</span></span>      | <span data-ttu-id="5e07c-117">1.2.840.113556.1.4.806</span><span class="sxs-lookup"><span data-stu-id="5e07c-117">1.2.840.113556.1.4.806</span></span>               |
| <span data-ttu-id="5e07c-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5e07c-118">System-Id-Guid</span></span>    | <span data-ttu-id="5e07c-119">8ld044e3-771l-11d1-aeae-0000f 80367c1</span><span class="sxs-lookup"><span data-stu-id="5e07c-119">8fd044e3-771f-11d1-aeae-0000f80367c1</span></span> |
| <span data-ttu-id="5e07c-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e07c-120">Syntax</span></span>            | [<span data-ttu-id="5e07c-121">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="5e07c-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="5e07c-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="5e07c-122">Implementations</span></span>

-   [<span data-ttu-id="5e07c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5e07c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5e07c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5e07c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5e07c-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5e07c-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5e07c-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5e07c-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5e07c-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5e07c-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5e07c-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5e07c-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5e07c-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5e07c-129">Windows 2000 Server</span></span>



| <span data-ttu-id="5e07c-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5e07c-130">Entry</span></span> | <span data-ttu-id="5e07c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="5e07c-131">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="5e07c-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5e07c-132">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="5e07c-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e07c-133">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="5e07c-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e07c-134">System-Only</span></span>            | <span data-ttu-id="5e07c-135">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-135">False</span></span>                                                      |
| <span data-ttu-id="5e07c-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5e07c-136">Is-Single-Valued</span></span>       | <span data-ttu-id="5e07c-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="5e07c-137">True</span></span>                                                       |
| <span data-ttu-id="5e07c-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5e07c-138">Is Indexed</span></span>             | <span data-ttu-id="5e07c-139">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-139">False</span></span>                                                      |
| <span data-ttu-id="5e07c-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5e07c-140">In Global Catalog</span></span>      | <span data-ttu-id="5e07c-141">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-141">False</span></span>                                                      |
| <span data-ttu-id="5e07c-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5e07c-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e07c-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5e07c-143">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="5e07c-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e07c-144">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="5e07c-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e07c-145">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="5e07c-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e07c-146">Search-Flags</span></span>           | <span data-ttu-id="5e07c-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5e07c-147">0x00000000</span></span>                                                 |
| <span data-ttu-id="5e07c-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e07c-148">System-Flags</span></span>           | <span data-ttu-id="5e07c-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e07c-149">0x00000010</span></span>                                                 |
| <span data-ttu-id="5e07c-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5e07c-150">Classes used in</span></span>        | [<span data-ttu-id="5e07c-151">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="5e07c-151">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5e07c-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5e07c-152">Windows Server 2003</span></span>



| <span data-ttu-id="5e07c-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5e07c-153">Entry</span></span> | <span data-ttu-id="5e07c-154">Wert</span><span class="sxs-lookup"><span data-stu-id="5e07c-154">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="5e07c-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5e07c-155">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="5e07c-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e07c-156">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="5e07c-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e07c-157">System-Only</span></span>            | <span data-ttu-id="5e07c-158">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-158">False</span></span>                                                      |
| <span data-ttu-id="5e07c-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5e07c-159">Is-Single-Valued</span></span>       | <span data-ttu-id="5e07c-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="5e07c-160">True</span></span>                                                       |
| <span data-ttu-id="5e07c-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5e07c-161">Is Indexed</span></span>             | <span data-ttu-id="5e07c-162">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-162">False</span></span>                                                      |
| <span data-ttu-id="5e07c-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5e07c-163">In Global Catalog</span></span>      | <span data-ttu-id="5e07c-164">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-164">False</span></span>                                                      |
| <span data-ttu-id="5e07c-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5e07c-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e07c-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5e07c-166">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="5e07c-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e07c-167">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="5e07c-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e07c-168">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="5e07c-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e07c-169">Search-Flags</span></span>           | <span data-ttu-id="5e07c-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5e07c-170">0x00000000</span></span>                                                 |
| <span data-ttu-id="5e07c-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e07c-171">System-Flags</span></span>           | <span data-ttu-id="5e07c-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e07c-172">0x00000010</span></span>                                                 |
| <span data-ttu-id="5e07c-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5e07c-173">Classes used in</span></span>        | [<span data-ttu-id="5e07c-174">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="5e07c-174">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5e07c-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5e07c-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5e07c-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5e07c-176">Entry</span></span> | <span data-ttu-id="5e07c-177">Wert</span><span class="sxs-lookup"><span data-stu-id="5e07c-177">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="5e07c-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5e07c-178">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="5e07c-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e07c-179">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="5e07c-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e07c-180">System-Only</span></span>            | <span data-ttu-id="5e07c-181">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-181">False</span></span>                                                      |
| <span data-ttu-id="5e07c-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5e07c-182">Is-Single-Valued</span></span>       | <span data-ttu-id="5e07c-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="5e07c-183">True</span></span>                                                       |
| <span data-ttu-id="5e07c-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5e07c-184">Is Indexed</span></span>             | <span data-ttu-id="5e07c-185">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-185">False</span></span>                                                      |
| <span data-ttu-id="5e07c-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5e07c-186">In Global Catalog</span></span>      | <span data-ttu-id="5e07c-187">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-187">False</span></span>                                                      |
| <span data-ttu-id="5e07c-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5e07c-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e07c-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5e07c-189">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="5e07c-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e07c-190">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="5e07c-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e07c-191">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="5e07c-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e07c-192">Search-Flags</span></span>           | <span data-ttu-id="5e07c-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5e07c-193">0x00000000</span></span>                                                 |
| <span data-ttu-id="5e07c-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e07c-194">System-Flags</span></span>           | <span data-ttu-id="5e07c-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e07c-195">0x00000010</span></span>                                                 |
| <span data-ttu-id="5e07c-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5e07c-196">Classes used in</span></span>        | [<span data-ttu-id="5e07c-197">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="5e07c-197">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5e07c-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e07c-198">Windows Server 2008</span></span>



| <span data-ttu-id="5e07c-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5e07c-199">Entry</span></span> | <span data-ttu-id="5e07c-200">Wert</span><span class="sxs-lookup"><span data-stu-id="5e07c-200">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="5e07c-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5e07c-201">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="5e07c-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e07c-202">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="5e07c-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e07c-203">System-Only</span></span>            | <span data-ttu-id="5e07c-204">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-204">False</span></span>                                                      |
| <span data-ttu-id="5e07c-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5e07c-205">Is-Single-Valued</span></span>       | <span data-ttu-id="5e07c-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="5e07c-206">True</span></span>                                                       |
| <span data-ttu-id="5e07c-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5e07c-207">Is Indexed</span></span>             | <span data-ttu-id="5e07c-208">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-208">False</span></span>                                                      |
| <span data-ttu-id="5e07c-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5e07c-209">In Global Catalog</span></span>      | <span data-ttu-id="5e07c-210">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-210">False</span></span>                                                      |
| <span data-ttu-id="5e07c-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5e07c-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e07c-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5e07c-212">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="5e07c-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e07c-213">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="5e07c-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e07c-214">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="5e07c-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e07c-215">Search-Flags</span></span>           | <span data-ttu-id="5e07c-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5e07c-216">0x00000000</span></span>                                                 |
| <span data-ttu-id="5e07c-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e07c-217">System-Flags</span></span>           | <span data-ttu-id="5e07c-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e07c-218">0x00000010</span></span>                                                 |
| <span data-ttu-id="5e07c-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5e07c-219">Classes used in</span></span>        | [<span data-ttu-id="5e07c-220">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="5e07c-220">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5e07c-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5e07c-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5e07c-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5e07c-222">Entry</span></span> | <span data-ttu-id="5e07c-223">Wert</span><span class="sxs-lookup"><span data-stu-id="5e07c-223">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="5e07c-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5e07c-224">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="5e07c-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e07c-225">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="5e07c-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e07c-226">System-Only</span></span>            | <span data-ttu-id="5e07c-227">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-227">False</span></span>                                                      |
| <span data-ttu-id="5e07c-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5e07c-228">Is-Single-Valued</span></span>       | <span data-ttu-id="5e07c-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="5e07c-229">True</span></span>                                                       |
| <span data-ttu-id="5e07c-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5e07c-230">Is Indexed</span></span>             | <span data-ttu-id="5e07c-231">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-231">False</span></span>                                                      |
| <span data-ttu-id="5e07c-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5e07c-232">In Global Catalog</span></span>      | <span data-ttu-id="5e07c-233">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-233">False</span></span>                                                      |
| <span data-ttu-id="5e07c-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5e07c-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e07c-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5e07c-235">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="5e07c-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e07c-236">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="5e07c-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e07c-237">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="5e07c-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e07c-238">Search-Flags</span></span>           | <span data-ttu-id="5e07c-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5e07c-239">0x00000000</span></span>                                                 |
| <span data-ttu-id="5e07c-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e07c-240">System-Flags</span></span>           | <span data-ttu-id="5e07c-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e07c-241">0x00000010</span></span>                                                 |
| <span data-ttu-id="5e07c-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5e07c-242">Classes used in</span></span>        | [<span data-ttu-id="5e07c-243">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="5e07c-243">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5e07c-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5e07c-244">Windows Server 2012</span></span>



| <span data-ttu-id="5e07c-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5e07c-245">Entry</span></span> | <span data-ttu-id="5e07c-246">Wert</span><span class="sxs-lookup"><span data-stu-id="5e07c-246">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="5e07c-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5e07c-247">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="5e07c-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5e07c-248">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="5e07c-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="5e07c-249">System-Only</span></span>            | <span data-ttu-id="5e07c-250">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-250">False</span></span>                                                      |
| <span data-ttu-id="5e07c-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5e07c-251">Is-Single-Valued</span></span>       | <span data-ttu-id="5e07c-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="5e07c-252">True</span></span>                                                       |
| <span data-ttu-id="5e07c-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5e07c-253">Is Indexed</span></span>             | <span data-ttu-id="5e07c-254">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-254">False</span></span>                                                      |
| <span data-ttu-id="5e07c-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5e07c-255">In Global Catalog</span></span>      | <span data-ttu-id="5e07c-256">False</span><span class="sxs-lookup"><span data-stu-id="5e07c-256">False</span></span>                                                      |
| <span data-ttu-id="5e07c-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5e07c-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="5e07c-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5e07c-258">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="5e07c-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5e07c-259">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="5e07c-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5e07c-260">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="5e07c-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5e07c-261">Search-Flags</span></span>           | <span data-ttu-id="5e07c-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5e07c-262">0x00000000</span></span>                                                 |
| <span data-ttu-id="5e07c-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5e07c-263">System-Flags</span></span>           | <span data-ttu-id="5e07c-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5e07c-264">0x00000010</span></span>                                                 |
| <span data-ttu-id="5e07c-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5e07c-265">Classes used in</span></span>        | [<span data-ttu-id="5e07c-266">**Anzeige-Spezifizierer**</span><span class="sxs-lookup"><span data-stu-id="5e07c-266">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





