---
title: Extension-Name-Attribut
description: Der Name einer Eigenschaften Seite, die zum Erweitern der Benutzeroberfläche eines Verzeichnis Objekts verwendet wird.
ms.assetid: 7afa3363-00ac-4651-8a5c-b36b4ee8bf88
ms.tgt_platform: multiple
keywords:
- AD-Schema für Extension-Name-Attribut
- AD-Schema für das ExtensionName-Attribut
topic_type:
- apiref
api_name:
- Extension-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 841685edbafbc761b1531f29f16d45657b57011d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106340026"
---
# <a name="extension-name-attribute"></a><span data-ttu-id="1d25c-105">Extension-Name-Attribut</span><span class="sxs-lookup"><span data-stu-id="1d25c-105">Extension-Name attribute</span></span>

<span data-ttu-id="1d25c-106">Der Name einer Eigenschaften Seite, die zum Erweitern der Benutzeroberfläche eines Verzeichnis Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d25c-106">The name of a property page used to extend the UI of a directory object.</span></span>



| <span data-ttu-id="1d25c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1d25c-107">Entry</span></span> | <span data-ttu-id="1d25c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="1d25c-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="1d25c-109">CN</span><span class="sxs-lookup"><span data-stu-id="1d25c-109">CN</span></span>                | <span data-ttu-id="1d25c-110">Extension-Name</span><span class="sxs-lookup"><span data-stu-id="1d25c-110">Extension-Name</span></span>                              |
| <span data-ttu-id="1d25c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1d25c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1d25c-112">extensionName</span><span class="sxs-lookup"><span data-stu-id="1d25c-112">extensionName</span></span>                               |
| <span data-ttu-id="1d25c-113">Size</span><span class="sxs-lookup"><span data-stu-id="1d25c-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="1d25c-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="1d25c-114">Update Privilege</span></span>  | <span data-ttu-id="1d25c-115">Der Ersteller des Erweiterungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="1d25c-115">The creator of the extension object.</span></span>        |
| <span data-ttu-id="1d25c-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="1d25c-116">Update Frequency</span></span>  | <span data-ttu-id="1d25c-117">Immer dann, wenn eine neue Benutzeroberflächen Erweiterung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1d25c-117">Whenever a new UI extension is created.</span></span>     |
| <span data-ttu-id="1d25c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1d25c-118">Attribute-Id</span></span>      | <span data-ttu-id="1d25c-119">1.2.840.113556.1.2.227</span><span class="sxs-lookup"><span data-stu-id="1d25c-119">1.2.840.113556.1.2.227</span></span>                      |
| <span data-ttu-id="1d25c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1d25c-120">System-Id-Guid</span></span>    | <span data-ttu-id="1d25c-121">bf967972-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1d25c-121">bf967972-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="1d25c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d25c-122">Syntax</span></span>            | [<span data-ttu-id="1d25c-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1d25c-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="1d25c-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="1d25c-124">Implementations</span></span>

-   [<span data-ttu-id="1d25c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1d25c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1d25c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1d25c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1d25c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1d25c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1d25c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1d25c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1d25c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1d25c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1d25c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1d25c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1d25c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1d25c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="1d25c-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1d25c-132">Entry</span></span> | <span data-ttu-id="1d25c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="1d25c-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d25c-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1d25c-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d25c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d25c-135">MAPI-Id</span></span>                | <span data-ttu-id="1d25c-136">0x80a9</span><span class="sxs-lookup"><span data-stu-id="1d25c-136">0x80A9</span></span>                          |
| <span data-ttu-id="1d25c-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d25c-137">System-Only</span></span>            | <span data-ttu-id="1d25c-138">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-138">False</span></span>                           |
| <span data-ttu-id="1d25c-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1d25c-139">Is-Single-Valued</span></span>       | <span data-ttu-id="1d25c-140">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-140">False</span></span>                           |
| <span data-ttu-id="1d25c-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1d25c-141">Is Indexed</span></span>             | <span data-ttu-id="1d25c-142">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-142">False</span></span>                           |
| <span data-ttu-id="1d25c-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1d25c-143">In Global Catalog</span></span>      | <span data-ttu-id="1d25c-144">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-144">False</span></span>                           |
| <span data-ttu-id="1d25c-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1d25c-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d25c-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1d25c-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d25c-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d25c-147">Range-Lower</span></span>            | <span data-ttu-id="1d25c-148">1</span><span class="sxs-lookup"><span data-stu-id="1d25c-148">1</span></span>                               |
| <span data-ttu-id="1d25c-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d25c-149">Range-Upper</span></span>            | <span data-ttu-id="1d25c-150">255</span><span class="sxs-lookup"><span data-stu-id="1d25c-150">255</span></span>                             |
| <span data-ttu-id="1d25c-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d25c-151">Search-Flags</span></span>           | <span data-ttu-id="1d25c-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d25c-152">0x00000000</span></span>                      |
| <span data-ttu-id="1d25c-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d25c-153">System-Flags</span></span>           | <span data-ttu-id="1d25c-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d25c-154">0x00000010</span></span>                      |
| <span data-ttu-id="1d25c-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1d25c-155">Classes used in</span></span>        | [<span data-ttu-id="1d25c-156">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1d25c-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1d25c-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1d25c-157">Windows Server 2003</span></span>



| <span data-ttu-id="1d25c-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1d25c-158">Entry</span></span> | <span data-ttu-id="1d25c-159">Wert</span><span class="sxs-lookup"><span data-stu-id="1d25c-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d25c-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1d25c-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d25c-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d25c-161">MAPI-Id</span></span>                | <span data-ttu-id="1d25c-162">0x80a9</span><span class="sxs-lookup"><span data-stu-id="1d25c-162">0x80A9</span></span>                          |
| <span data-ttu-id="1d25c-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d25c-163">System-Only</span></span>            | <span data-ttu-id="1d25c-164">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-164">False</span></span>                           |
| <span data-ttu-id="1d25c-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1d25c-165">Is-Single-Valued</span></span>       | <span data-ttu-id="1d25c-166">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-166">False</span></span>                           |
| <span data-ttu-id="1d25c-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1d25c-167">Is Indexed</span></span>             | <span data-ttu-id="1d25c-168">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-168">False</span></span>                           |
| <span data-ttu-id="1d25c-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1d25c-169">In Global Catalog</span></span>      | <span data-ttu-id="1d25c-170">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-170">False</span></span>                           |
| <span data-ttu-id="1d25c-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1d25c-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d25c-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1d25c-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d25c-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d25c-173">Range-Lower</span></span>            | <span data-ttu-id="1d25c-174">1</span><span class="sxs-lookup"><span data-stu-id="1d25c-174">1</span></span>                               |
| <span data-ttu-id="1d25c-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d25c-175">Range-Upper</span></span>            | <span data-ttu-id="1d25c-176">255</span><span class="sxs-lookup"><span data-stu-id="1d25c-176">255</span></span>                             |
| <span data-ttu-id="1d25c-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d25c-177">Search-Flags</span></span>           | <span data-ttu-id="1d25c-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d25c-178">0x00000000</span></span>                      |
| <span data-ttu-id="1d25c-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d25c-179">System-Flags</span></span>           | <span data-ttu-id="1d25c-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d25c-180">0x00000010</span></span>                      |
| <span data-ttu-id="1d25c-181">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1d25c-181">Classes used in</span></span>        | [<span data-ttu-id="1d25c-182">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1d25c-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1d25c-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1d25c-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1d25c-184">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1d25c-184">Entry</span></span> | <span data-ttu-id="1d25c-185">Wert</span><span class="sxs-lookup"><span data-stu-id="1d25c-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d25c-186">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1d25c-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d25c-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d25c-187">MAPI-Id</span></span>                | <span data-ttu-id="1d25c-188">0x80a9</span><span class="sxs-lookup"><span data-stu-id="1d25c-188">0x80A9</span></span>                          |
| <span data-ttu-id="1d25c-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d25c-189">System-Only</span></span>            | <span data-ttu-id="1d25c-190">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-190">False</span></span>                           |
| <span data-ttu-id="1d25c-191">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1d25c-191">Is-Single-Valued</span></span>       | <span data-ttu-id="1d25c-192">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-192">False</span></span>                           |
| <span data-ttu-id="1d25c-193">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1d25c-193">Is Indexed</span></span>             | <span data-ttu-id="1d25c-194">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-194">False</span></span>                           |
| <span data-ttu-id="1d25c-195">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1d25c-195">In Global Catalog</span></span>      | <span data-ttu-id="1d25c-196">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-196">False</span></span>                           |
| <span data-ttu-id="1d25c-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1d25c-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d25c-198">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1d25c-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d25c-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d25c-199">Range-Lower</span></span>            | <span data-ttu-id="1d25c-200">1</span><span class="sxs-lookup"><span data-stu-id="1d25c-200">1</span></span>                               |
| <span data-ttu-id="1d25c-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d25c-201">Range-Upper</span></span>            | <span data-ttu-id="1d25c-202">255</span><span class="sxs-lookup"><span data-stu-id="1d25c-202">255</span></span>                             |
| <span data-ttu-id="1d25c-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d25c-203">Search-Flags</span></span>           | <span data-ttu-id="1d25c-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d25c-204">0x00000000</span></span>                      |
| <span data-ttu-id="1d25c-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d25c-205">System-Flags</span></span>           | <span data-ttu-id="1d25c-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d25c-206">0x00000010</span></span>                      |
| <span data-ttu-id="1d25c-207">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1d25c-207">Classes used in</span></span>        | [<span data-ttu-id="1d25c-208">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1d25c-208">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1d25c-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d25c-209">Windows Server 2008</span></span>



| <span data-ttu-id="1d25c-210">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1d25c-210">Entry</span></span> | <span data-ttu-id="1d25c-211">Wert</span><span class="sxs-lookup"><span data-stu-id="1d25c-211">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d25c-212">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1d25c-212">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d25c-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d25c-213">MAPI-Id</span></span>                | <span data-ttu-id="1d25c-214">0x80a9</span><span class="sxs-lookup"><span data-stu-id="1d25c-214">0x80A9</span></span>                          |
| <span data-ttu-id="1d25c-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d25c-215">System-Only</span></span>            | <span data-ttu-id="1d25c-216">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-216">False</span></span>                           |
| <span data-ttu-id="1d25c-217">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1d25c-217">Is-Single-Valued</span></span>       | <span data-ttu-id="1d25c-218">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-218">False</span></span>                           |
| <span data-ttu-id="1d25c-219">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1d25c-219">Is Indexed</span></span>             | <span data-ttu-id="1d25c-220">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-220">False</span></span>                           |
| <span data-ttu-id="1d25c-221">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1d25c-221">In Global Catalog</span></span>      | <span data-ttu-id="1d25c-222">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-222">False</span></span>                           |
| <span data-ttu-id="1d25c-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1d25c-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d25c-224">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1d25c-224">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d25c-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d25c-225">Range-Lower</span></span>            | <span data-ttu-id="1d25c-226">1</span><span class="sxs-lookup"><span data-stu-id="1d25c-226">1</span></span>                               |
| <span data-ttu-id="1d25c-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d25c-227">Range-Upper</span></span>            | <span data-ttu-id="1d25c-228">255</span><span class="sxs-lookup"><span data-stu-id="1d25c-228">255</span></span>                             |
| <span data-ttu-id="1d25c-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d25c-229">Search-Flags</span></span>           | <span data-ttu-id="1d25c-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d25c-230">0x00000000</span></span>                      |
| <span data-ttu-id="1d25c-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d25c-231">System-Flags</span></span>           | <span data-ttu-id="1d25c-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d25c-232">0x00000010</span></span>                      |
| <span data-ttu-id="1d25c-233">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1d25c-233">Classes used in</span></span>        | [<span data-ttu-id="1d25c-234">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1d25c-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1d25c-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1d25c-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1d25c-236">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1d25c-236">Entry</span></span> | <span data-ttu-id="1d25c-237">Wert</span><span class="sxs-lookup"><span data-stu-id="1d25c-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d25c-238">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1d25c-238">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d25c-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d25c-239">MAPI-Id</span></span>                | <span data-ttu-id="1d25c-240">0x80a9</span><span class="sxs-lookup"><span data-stu-id="1d25c-240">0x80A9</span></span>                          |
| <span data-ttu-id="1d25c-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d25c-241">System-Only</span></span>            | <span data-ttu-id="1d25c-242">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-242">False</span></span>                           |
| <span data-ttu-id="1d25c-243">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1d25c-243">Is-Single-Valued</span></span>       | <span data-ttu-id="1d25c-244">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-244">False</span></span>                           |
| <span data-ttu-id="1d25c-245">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1d25c-245">Is Indexed</span></span>             | <span data-ttu-id="1d25c-246">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-246">False</span></span>                           |
| <span data-ttu-id="1d25c-247">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1d25c-247">In Global Catalog</span></span>      | <span data-ttu-id="1d25c-248">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-248">False</span></span>                           |
| <span data-ttu-id="1d25c-249">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1d25c-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d25c-250">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1d25c-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d25c-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d25c-251">Range-Lower</span></span>            | <span data-ttu-id="1d25c-252">1</span><span class="sxs-lookup"><span data-stu-id="1d25c-252">1</span></span>                               |
| <span data-ttu-id="1d25c-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d25c-253">Range-Upper</span></span>            | <span data-ttu-id="1d25c-254">255</span><span class="sxs-lookup"><span data-stu-id="1d25c-254">255</span></span>                             |
| <span data-ttu-id="1d25c-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d25c-255">Search-Flags</span></span>           | <span data-ttu-id="1d25c-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d25c-256">0x00000000</span></span>                      |
| <span data-ttu-id="1d25c-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d25c-257">System-Flags</span></span>           | <span data-ttu-id="1d25c-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d25c-258">0x00000010</span></span>                      |
| <span data-ttu-id="1d25c-259">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1d25c-259">Classes used in</span></span>        | [<span data-ttu-id="1d25c-260">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1d25c-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1d25c-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1d25c-261">Windows Server 2012</span></span>



| <span data-ttu-id="1d25c-262">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1d25c-262">Entry</span></span> | <span data-ttu-id="1d25c-263">Wert</span><span class="sxs-lookup"><span data-stu-id="1d25c-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1d25c-264">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1d25c-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1d25c-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d25c-265">MAPI-Id</span></span>                | <span data-ttu-id="1d25c-266">0x80a9</span><span class="sxs-lookup"><span data-stu-id="1d25c-266">0x80A9</span></span>                          |
| <span data-ttu-id="1d25c-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d25c-267">System-Only</span></span>            | <span data-ttu-id="1d25c-268">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-268">False</span></span>                           |
| <span data-ttu-id="1d25c-269">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1d25c-269">Is-Single-Valued</span></span>       | <span data-ttu-id="1d25c-270">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-270">False</span></span>                           |
| <span data-ttu-id="1d25c-271">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1d25c-271">Is Indexed</span></span>             | <span data-ttu-id="1d25c-272">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-272">False</span></span>                           |
| <span data-ttu-id="1d25c-273">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1d25c-273">In Global Catalog</span></span>      | <span data-ttu-id="1d25c-274">False</span><span class="sxs-lookup"><span data-stu-id="1d25c-274">False</span></span>                           |
| <span data-ttu-id="1d25c-275">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1d25c-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d25c-276">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1d25c-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1d25c-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d25c-277">Range-Lower</span></span>            | <span data-ttu-id="1d25c-278">1</span><span class="sxs-lookup"><span data-stu-id="1d25c-278">1</span></span>                               |
| <span data-ttu-id="1d25c-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d25c-279">Range-Upper</span></span>            | <span data-ttu-id="1d25c-280">255</span><span class="sxs-lookup"><span data-stu-id="1d25c-280">255</span></span>                             |
| <span data-ttu-id="1d25c-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d25c-281">Search-Flags</span></span>           | <span data-ttu-id="1d25c-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d25c-282">0x00000000</span></span>                      |
| <span data-ttu-id="1d25c-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d25c-283">System-Flags</span></span>           | <span data-ttu-id="1d25c-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d25c-284">0x00000010</span></span>                      |
| <span data-ttu-id="1d25c-285">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1d25c-285">Classes used in</span></span>        | [<span data-ttu-id="1d25c-286">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="1d25c-286">**Top**</span></span>](c-top.md)<br/> |



 

 





