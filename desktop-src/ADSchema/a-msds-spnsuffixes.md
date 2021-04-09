---
title: ms-DS-SPN-Suffixes-Attribut
description: Dieses Attribut beschreibt die Suffixe von DNS-Hostnamen, die von Servern in der Gesamtstruktur verwendet werden. Diese DNS-Suffixe werden für andere Gesamtstrukturen freigegeben, die über eine Gesamtstruktur übergreifende Vertrauensstellung mit dieser Gesamtstruktur verfügen.
ms.assetid: 56153832-1228-419f-99d4-eb1ce3edc867
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-SPN-Suffixe-Attribut
- AD-Schema des msDS-spnsuffixes-Attributs
topic_type:
- apiref
api_name:
- ms-DS-SPN-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91f7ce8c92e8a81437d90bb0d80383b9ad334ee
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957508"
---
# <a name="ms-ds-spn-suffixes-attribute"></a><span data-ttu-id="5f86a-106">ms-DS-SPN-Suffixes-Attribut</span><span class="sxs-lookup"><span data-stu-id="5f86a-106">ms-DS-SPN-Suffixes attribute</span></span>

<span data-ttu-id="5f86a-107">Dieses Attribut beschreibt die Suffixe von DNS-Hostnamen, die von Servern in der Gesamtstruktur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f86a-107">This attribute describes the suffixes of DNS host names used by servers in the forest.</span></span> <span data-ttu-id="5f86a-108">Diese DNS-Suffixe werden für andere Gesamtstrukturen freigegeben, die über eine Gesamtstruktur übergreifende Vertrauensstellung mit dieser Gesamtstruktur verfügen.</span><span class="sxs-lookup"><span data-stu-id="5f86a-108">These DNS suffixes will be shared with other forests that have cross-forest trust with this forest.</span></span>



| <span data-ttu-id="5f86a-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5f86a-109">Entry</span></span> | <span data-ttu-id="5f86a-110">Wert</span><span class="sxs-lookup"><span data-stu-id="5f86a-110">Value</span></span> |
|-------------------|----------------------------------------------|
| <span data-ttu-id="5f86a-111">CN</span><span class="sxs-lookup"><span data-stu-id="5f86a-111">CN</span></span>                | <span data-ttu-id="5f86a-112">ms-DS-SPN-Suffixe</span><span class="sxs-lookup"><span data-stu-id="5f86a-112">ms-DS-SPN-Suffixes</span></span>                           |
| <span data-ttu-id="5f86a-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5f86a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5f86a-114">MSDS-spnsuffixes</span><span class="sxs-lookup"><span data-stu-id="5f86a-114">msDS-SPNSuffixes</span></span>                             |
| <span data-ttu-id="5f86a-115">Size</span><span class="sxs-lookup"><span data-stu-id="5f86a-115">Size</span></span>              | <span data-ttu-id="5f86a-116">255 Bytes</span><span class="sxs-lookup"><span data-stu-id="5f86a-116">255 bytes</span></span>                                    |
| <span data-ttu-id="5f86a-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5f86a-117">Update Privilege</span></span>  | <span data-ttu-id="5f86a-118">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="5f86a-118">Domain administrator</span></span>                         |
| <span data-ttu-id="5f86a-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="5f86a-119">Update Frequency</span></span>  | <span data-ttu-id="5f86a-120">Wenn Server in der Gesamtstruktur ein neues Suffix erhalten.</span><span class="sxs-lookup"><span data-stu-id="5f86a-120">When servers in the forest get a new suffix.</span></span> |
| <span data-ttu-id="5f86a-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5f86a-121">Attribute-Id</span></span>      | <span data-ttu-id="5f86a-122">1.2.840.113556.1.4.1715</span><span class="sxs-lookup"><span data-stu-id="5f86a-122">1.2.840.113556.1.4.1715</span></span>                      |
| <span data-ttu-id="5f86a-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5f86a-123">System-Id-Guid</span></span>    | <span data-ttu-id="5f86a-124">789ee1eb-8c8e-4e4c-8cec-79b31b7617b5</span><span class="sxs-lookup"><span data-stu-id="5f86a-124">789ee1eb-8c8e-4e4c-8cec-79b31b7617b5</span></span>         |
| <span data-ttu-id="5f86a-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f86a-125">Syntax</span></span>            | [<span data-ttu-id="5f86a-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5f86a-126">**String(Unicode)**</span></span>](s-string-unicode.md)  |



## <a name="implementations"></a><span data-ttu-id="5f86a-127">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="5f86a-127">Implementations</span></span>

-   [<span data-ttu-id="5f86a-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5f86a-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5f86a-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5f86a-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5f86a-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5f86a-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5f86a-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5f86a-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5f86a-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5f86a-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="5f86a-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5f86a-133">Windows Server 2003</span></span>



| <span data-ttu-id="5f86a-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5f86a-134">Entry</span></span> | <span data-ttu-id="5f86a-135">Wert</span><span class="sxs-lookup"><span data-stu-id="5f86a-135">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5f86a-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5f86a-136">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5f86a-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f86a-137">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5f86a-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f86a-138">System-Only</span></span>            | <span data-ttu-id="5f86a-139">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-139">False</span></span>                                                         |
| <span data-ttu-id="5f86a-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5f86a-140">Is-Single-Valued</span></span>       | <span data-ttu-id="5f86a-141">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-141">False</span></span>                                                         |
| <span data-ttu-id="5f86a-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5f86a-142">Is Indexed</span></span>             | <span data-ttu-id="5f86a-143">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-143">False</span></span>                                                         |
| <span data-ttu-id="5f86a-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5f86a-144">In Global Catalog</span></span>      | <span data-ttu-id="5f86a-145">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-145">False</span></span>                                                         |
| <span data-ttu-id="5f86a-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5f86a-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f86a-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5f86a-147">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="5f86a-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f86a-148">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="5f86a-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f86a-149">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="5f86a-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f86a-150">Search-Flags</span></span>           | <span data-ttu-id="5f86a-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f86a-151">0x00000000</span></span>                                                    |
| <span data-ttu-id="5f86a-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f86a-152">System-Flags</span></span>           | <span data-ttu-id="5f86a-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f86a-153">0x00000010</span></span>                                                    |
| <span data-ttu-id="5f86a-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5f86a-154">Classes used in</span></span>        | [<span data-ttu-id="5f86a-155">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="5f86a-155">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5f86a-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5f86a-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5f86a-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5f86a-157">Entry</span></span> | <span data-ttu-id="5f86a-158">Wert</span><span class="sxs-lookup"><span data-stu-id="5f86a-158">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5f86a-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5f86a-159">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5f86a-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f86a-160">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5f86a-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f86a-161">System-Only</span></span>            | <span data-ttu-id="5f86a-162">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-162">False</span></span>                                                         |
| <span data-ttu-id="5f86a-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5f86a-163">Is-Single-Valued</span></span>       | <span data-ttu-id="5f86a-164">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-164">False</span></span>                                                         |
| <span data-ttu-id="5f86a-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5f86a-165">Is Indexed</span></span>             | <span data-ttu-id="5f86a-166">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-166">False</span></span>                                                         |
| <span data-ttu-id="5f86a-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5f86a-167">In Global Catalog</span></span>      | <span data-ttu-id="5f86a-168">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-168">False</span></span>                                                         |
| <span data-ttu-id="5f86a-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5f86a-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f86a-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5f86a-170">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="5f86a-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f86a-171">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="5f86a-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f86a-172">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="5f86a-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f86a-173">Search-Flags</span></span>           | <span data-ttu-id="5f86a-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f86a-174">0x00000000</span></span>                                                    |
| <span data-ttu-id="5f86a-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f86a-175">System-Flags</span></span>           | <span data-ttu-id="5f86a-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f86a-176">0x00000010</span></span>                                                    |
| <span data-ttu-id="5f86a-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5f86a-177">Classes used in</span></span>        | [<span data-ttu-id="5f86a-178">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="5f86a-178">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5f86a-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f86a-179">Windows Server 2008</span></span>



| <span data-ttu-id="5f86a-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5f86a-180">Entry</span></span> | <span data-ttu-id="5f86a-181">Wert</span><span class="sxs-lookup"><span data-stu-id="5f86a-181">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5f86a-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5f86a-182">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5f86a-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f86a-183">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5f86a-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f86a-184">System-Only</span></span>            | <span data-ttu-id="5f86a-185">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-185">False</span></span>                                                         |
| <span data-ttu-id="5f86a-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5f86a-186">Is-Single-Valued</span></span>       | <span data-ttu-id="5f86a-187">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-187">False</span></span>                                                         |
| <span data-ttu-id="5f86a-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5f86a-188">Is Indexed</span></span>             | <span data-ttu-id="5f86a-189">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-189">False</span></span>                                                         |
| <span data-ttu-id="5f86a-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5f86a-190">In Global Catalog</span></span>      | <span data-ttu-id="5f86a-191">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-191">False</span></span>                                                         |
| <span data-ttu-id="5f86a-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5f86a-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f86a-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5f86a-193">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="5f86a-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f86a-194">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="5f86a-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f86a-195">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="5f86a-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f86a-196">Search-Flags</span></span>           | <span data-ttu-id="5f86a-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f86a-197">0x00000000</span></span>                                                    |
| <span data-ttu-id="5f86a-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f86a-198">System-Flags</span></span>           | <span data-ttu-id="5f86a-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f86a-199">0x00000010</span></span>                                                    |
| <span data-ttu-id="5f86a-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5f86a-200">Classes used in</span></span>        | [<span data-ttu-id="5f86a-201">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="5f86a-201">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5f86a-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5f86a-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5f86a-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5f86a-203">Entry</span></span> | <span data-ttu-id="5f86a-204">Wert</span><span class="sxs-lookup"><span data-stu-id="5f86a-204">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5f86a-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5f86a-205">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5f86a-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f86a-206">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5f86a-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f86a-207">System-Only</span></span>            | <span data-ttu-id="5f86a-208">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-208">False</span></span>                                                         |
| <span data-ttu-id="5f86a-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5f86a-209">Is-Single-Valued</span></span>       | <span data-ttu-id="5f86a-210">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-210">False</span></span>                                                         |
| <span data-ttu-id="5f86a-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5f86a-211">Is Indexed</span></span>             | <span data-ttu-id="5f86a-212">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-212">False</span></span>                                                         |
| <span data-ttu-id="5f86a-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5f86a-213">In Global Catalog</span></span>      | <span data-ttu-id="5f86a-214">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-214">False</span></span>                                                         |
| <span data-ttu-id="5f86a-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5f86a-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f86a-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5f86a-216">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="5f86a-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f86a-217">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="5f86a-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f86a-218">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="5f86a-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f86a-219">Search-Flags</span></span>           | <span data-ttu-id="5f86a-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f86a-220">0x00000000</span></span>                                                    |
| <span data-ttu-id="5f86a-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f86a-221">System-Flags</span></span>           | <span data-ttu-id="5f86a-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f86a-222">0x00000010</span></span>                                                    |
| <span data-ttu-id="5f86a-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5f86a-223">Classes used in</span></span>        | [<span data-ttu-id="5f86a-224">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="5f86a-224">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5f86a-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5f86a-225">Windows Server 2012</span></span>



| <span data-ttu-id="5f86a-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5f86a-226">Entry</span></span> | <span data-ttu-id="5f86a-227">Wert</span><span class="sxs-lookup"><span data-stu-id="5f86a-227">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5f86a-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5f86a-228">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5f86a-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f86a-229">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5f86a-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f86a-230">System-Only</span></span>            | <span data-ttu-id="5f86a-231">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-231">False</span></span>                                                         |
| <span data-ttu-id="5f86a-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5f86a-232">Is-Single-Valued</span></span>       | <span data-ttu-id="5f86a-233">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-233">False</span></span>                                                         |
| <span data-ttu-id="5f86a-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5f86a-234">Is Indexed</span></span>             | <span data-ttu-id="5f86a-235">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-235">False</span></span>                                                         |
| <span data-ttu-id="5f86a-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5f86a-236">In Global Catalog</span></span>      | <span data-ttu-id="5f86a-237">False</span><span class="sxs-lookup"><span data-stu-id="5f86a-237">False</span></span>                                                         |
| <span data-ttu-id="5f86a-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5f86a-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f86a-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5f86a-239">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="5f86a-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f86a-240">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="5f86a-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f86a-241">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="5f86a-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f86a-242">Search-Flags</span></span>           | <span data-ttu-id="5f86a-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f86a-243">0x00000000</span></span>                                                    |
| <span data-ttu-id="5f86a-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f86a-244">System-Flags</span></span>           | <span data-ttu-id="5f86a-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f86a-245">0x00000010</span></span>                                                    |
| <span data-ttu-id="5f86a-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5f86a-246">Classes used in</span></span>        | [<span data-ttu-id="5f86a-247">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="5f86a-247">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





