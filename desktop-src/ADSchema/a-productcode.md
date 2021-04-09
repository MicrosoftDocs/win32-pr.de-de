---
title: Product-Code-Attribut
description: Dieses Attribut enthält einen eindeutigen Bezeichner für eine Anwendung für eine bestimmte Produktversion, die als Zeichen folgen-GUID dargestellt wird, z. b. \ 0034; 12345678-1234-1234-1234-123456789012 \ 0034;.
ms.assetid: 1fb50a4c-1a6a-4231-a6b2-92f6bc4a1ead
ms.tgt_platform: multiple
keywords:
- AD-Schema für Product-Code-Attribut
- ProductCode-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Product-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51dc874552fc819de4f9c58b23809b9f5662ee6e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957320"
---
# <a name="product-code-attribute"></a><span data-ttu-id="d689b-105">Product-Code-Attribut</span><span class="sxs-lookup"><span data-stu-id="d689b-105">Product-Code attribute</span></span>

<span data-ttu-id="d689b-106">Dieses Attribut enthält einen eindeutigen Bezeichner für eine Anwendung für eine bestimmte Produktversion, die als Zeichen folgen-GUID dargestellt wird, z {12345678-1234-1234-1234-123456789012} . b. "".</span><span class="sxs-lookup"><span data-stu-id="d689b-106">This attribute contains a unique identifier for an application for a particular product release, represented as a string GUID, for example "{12345678-1234-1234-1234-123456789012}".</span></span> <span data-ttu-id="d689b-107">Die in dieser GUID verwendeten Buchstaben müssen in Großbuchstaben angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d689b-107">Letters used in this GUID must be uppercase.</span></span> <span data-ttu-id="d689b-108">Diese ID muss für verschiedene Versionen und Sprachen variieren.</span><span class="sxs-lookup"><span data-stu-id="d689b-108">This ID must vary for different versions and languages.</span></span>



| <span data-ttu-id="d689b-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d689b-109">Entry</span></span> | <span data-ttu-id="d689b-110">Wert</span><span class="sxs-lookup"><span data-stu-id="d689b-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="d689b-111">CN</span><span class="sxs-lookup"><span data-stu-id="d689b-111">CN</span></span>                | <span data-ttu-id="d689b-112">Product-Code</span><span class="sxs-lookup"><span data-stu-id="d689b-112">Product-Code</span></span>                                          |
| <span data-ttu-id="d689b-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d689b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d689b-114">productCode</span><span class="sxs-lookup"><span data-stu-id="d689b-114">productCode</span></span>                                           |
| <span data-ttu-id="d689b-115">Size</span><span class="sxs-lookup"><span data-stu-id="d689b-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="d689b-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d689b-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="d689b-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="d689b-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="d689b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d689b-118">Attribute-Id</span></span>      | <span data-ttu-id="d689b-119">1.2.840.113556.1.4.818</span><span class="sxs-lookup"><span data-stu-id="d689b-119">1.2.840.113556.1.4.818</span></span>                                |
| <span data-ttu-id="d689b-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d689b-120">System-Id-Guid</span></span>    | <span data-ttu-id="d689b-121">d9e18317-8939-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d689b-121">d9e18317-8939-11d1-aebc-0000f80367c1</span></span>                  |
| <span data-ttu-id="d689b-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="d689b-122">Syntax</span></span>            | [<span data-ttu-id="d689b-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="d689b-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="d689b-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="d689b-124">Implementations</span></span>

-   [<span data-ttu-id="d689b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d689b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d689b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d689b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d689b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d689b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d689b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d689b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d689b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d689b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d689b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d689b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d689b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d689b-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d689b-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d689b-132">Entry</span></span> | <span data-ttu-id="d689b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="d689b-133">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d689b-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d689b-134">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d689b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d689b-135">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d689b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d689b-136">System-Only</span></span>            | <span data-ttu-id="d689b-137">False</span><span class="sxs-lookup"><span data-stu-id="d689b-137">False</span></span>                                                            |
| <span data-ttu-id="d689b-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d689b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d689b-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="d689b-139">True</span></span>                                                             |
| <span data-ttu-id="d689b-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d689b-140">Is Indexed</span></span>             | <span data-ttu-id="d689b-141">False</span><span class="sxs-lookup"><span data-stu-id="d689b-141">False</span></span>                                                            |
| <span data-ttu-id="d689b-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d689b-142">In Global Catalog</span></span>      | <span data-ttu-id="d689b-143">False</span><span class="sxs-lookup"><span data-stu-id="d689b-143">False</span></span>                                                            |
| <span data-ttu-id="d689b-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d689b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d689b-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d689b-145">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="d689b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d689b-146">Range-Lower</span></span>            | <span data-ttu-id="d689b-147">0</span><span class="sxs-lookup"><span data-stu-id="d689b-147">0</span></span>                                                                |
| <span data-ttu-id="d689b-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d689b-148">Range-Upper</span></span>            | <span data-ttu-id="d689b-149">16</span><span class="sxs-lookup"><span data-stu-id="d689b-149">16</span></span>                                                               |
| <span data-ttu-id="d689b-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d689b-150">Search-Flags</span></span>           | <span data-ttu-id="d689b-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d689b-151">0x00000000</span></span>                                                       |
| <span data-ttu-id="d689b-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d689b-152">System-Flags</span></span>           | <span data-ttu-id="d689b-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d689b-153">0x00000010</span></span>                                                       |
| <span data-ttu-id="d689b-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d689b-154">Classes used in</span></span>        | [<span data-ttu-id="d689b-155">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="d689b-155">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d689b-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d689b-156">Windows Server 2003</span></span>



| <span data-ttu-id="d689b-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d689b-157">Entry</span></span> | <span data-ttu-id="d689b-158">Wert</span><span class="sxs-lookup"><span data-stu-id="d689b-158">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d689b-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d689b-159">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d689b-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d689b-160">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d689b-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="d689b-161">System-Only</span></span>            | <span data-ttu-id="d689b-162">False</span><span class="sxs-lookup"><span data-stu-id="d689b-162">False</span></span>                                                            |
| <span data-ttu-id="d689b-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d689b-163">Is-Single-Valued</span></span>       | <span data-ttu-id="d689b-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="d689b-164">True</span></span>                                                             |
| <span data-ttu-id="d689b-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d689b-165">Is Indexed</span></span>             | <span data-ttu-id="d689b-166">False</span><span class="sxs-lookup"><span data-stu-id="d689b-166">False</span></span>                                                            |
| <span data-ttu-id="d689b-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d689b-167">In Global Catalog</span></span>      | <span data-ttu-id="d689b-168">False</span><span class="sxs-lookup"><span data-stu-id="d689b-168">False</span></span>                                                            |
| <span data-ttu-id="d689b-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d689b-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="d689b-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d689b-170">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="d689b-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d689b-171">Range-Lower</span></span>            | <span data-ttu-id="d689b-172">0</span><span class="sxs-lookup"><span data-stu-id="d689b-172">0</span></span>                                                                |
| <span data-ttu-id="d689b-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d689b-173">Range-Upper</span></span>            | <span data-ttu-id="d689b-174">16</span><span class="sxs-lookup"><span data-stu-id="d689b-174">16</span></span>                                                               |
| <span data-ttu-id="d689b-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d689b-175">Search-Flags</span></span>           | <span data-ttu-id="d689b-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d689b-176">0x00000000</span></span>                                                       |
| <span data-ttu-id="d689b-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d689b-177">System-Flags</span></span>           | <span data-ttu-id="d689b-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d689b-178">0x00000010</span></span>                                                       |
| <span data-ttu-id="d689b-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d689b-179">Classes used in</span></span>        | [<span data-ttu-id="d689b-180">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="d689b-180">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d689b-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d689b-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d689b-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d689b-182">Entry</span></span> | <span data-ttu-id="d689b-183">Wert</span><span class="sxs-lookup"><span data-stu-id="d689b-183">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d689b-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d689b-184">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d689b-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d689b-185">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d689b-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="d689b-186">System-Only</span></span>            | <span data-ttu-id="d689b-187">False</span><span class="sxs-lookup"><span data-stu-id="d689b-187">False</span></span>                                                            |
| <span data-ttu-id="d689b-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d689b-188">Is-Single-Valued</span></span>       | <span data-ttu-id="d689b-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="d689b-189">True</span></span>                                                             |
| <span data-ttu-id="d689b-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d689b-190">Is Indexed</span></span>             | <span data-ttu-id="d689b-191">False</span><span class="sxs-lookup"><span data-stu-id="d689b-191">False</span></span>                                                            |
| <span data-ttu-id="d689b-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d689b-192">In Global Catalog</span></span>      | <span data-ttu-id="d689b-193">False</span><span class="sxs-lookup"><span data-stu-id="d689b-193">False</span></span>                                                            |
| <span data-ttu-id="d689b-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d689b-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="d689b-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d689b-195">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="d689b-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d689b-196">Range-Lower</span></span>            | <span data-ttu-id="d689b-197">0</span><span class="sxs-lookup"><span data-stu-id="d689b-197">0</span></span>                                                                |
| <span data-ttu-id="d689b-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d689b-198">Range-Upper</span></span>            | <span data-ttu-id="d689b-199">16</span><span class="sxs-lookup"><span data-stu-id="d689b-199">16</span></span>                                                               |
| <span data-ttu-id="d689b-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d689b-200">Search-Flags</span></span>           | <span data-ttu-id="d689b-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d689b-201">0x00000000</span></span>                                                       |
| <span data-ttu-id="d689b-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d689b-202">System-Flags</span></span>           | <span data-ttu-id="d689b-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d689b-203">0x00000010</span></span>                                                       |
| <span data-ttu-id="d689b-204">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d689b-204">Classes used in</span></span>        | [<span data-ttu-id="d689b-205">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="d689b-205">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d689b-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d689b-206">Windows Server 2008</span></span>



| <span data-ttu-id="d689b-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d689b-207">Entry</span></span> | <span data-ttu-id="d689b-208">Wert</span><span class="sxs-lookup"><span data-stu-id="d689b-208">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d689b-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d689b-209">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d689b-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d689b-210">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d689b-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="d689b-211">System-Only</span></span>            | <span data-ttu-id="d689b-212">False</span><span class="sxs-lookup"><span data-stu-id="d689b-212">False</span></span>                                                            |
| <span data-ttu-id="d689b-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d689b-213">Is-Single-Valued</span></span>       | <span data-ttu-id="d689b-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="d689b-214">True</span></span>                                                             |
| <span data-ttu-id="d689b-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d689b-215">Is Indexed</span></span>             | <span data-ttu-id="d689b-216">False</span><span class="sxs-lookup"><span data-stu-id="d689b-216">False</span></span>                                                            |
| <span data-ttu-id="d689b-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d689b-217">In Global Catalog</span></span>      | <span data-ttu-id="d689b-218">False</span><span class="sxs-lookup"><span data-stu-id="d689b-218">False</span></span>                                                            |
| <span data-ttu-id="d689b-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d689b-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="d689b-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d689b-220">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="d689b-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d689b-221">Range-Lower</span></span>            | <span data-ttu-id="d689b-222">0</span><span class="sxs-lookup"><span data-stu-id="d689b-222">0</span></span>                                                                |
| <span data-ttu-id="d689b-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d689b-223">Range-Upper</span></span>            | <span data-ttu-id="d689b-224">16</span><span class="sxs-lookup"><span data-stu-id="d689b-224">16</span></span>                                                               |
| <span data-ttu-id="d689b-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d689b-225">Search-Flags</span></span>           | <span data-ttu-id="d689b-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d689b-226">0x00000000</span></span>                                                       |
| <span data-ttu-id="d689b-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d689b-227">System-Flags</span></span>           | <span data-ttu-id="d689b-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d689b-228">0x00000010</span></span>                                                       |
| <span data-ttu-id="d689b-229">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d689b-229">Classes used in</span></span>        | [<span data-ttu-id="d689b-230">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="d689b-230">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d689b-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d689b-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d689b-232">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d689b-232">Entry</span></span> | <span data-ttu-id="d689b-233">Wert</span><span class="sxs-lookup"><span data-stu-id="d689b-233">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d689b-234">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d689b-234">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d689b-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d689b-235">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d689b-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="d689b-236">System-Only</span></span>            | <span data-ttu-id="d689b-237">False</span><span class="sxs-lookup"><span data-stu-id="d689b-237">False</span></span>                                                            |
| <span data-ttu-id="d689b-238">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d689b-238">Is-Single-Valued</span></span>       | <span data-ttu-id="d689b-239">Richtig</span><span class="sxs-lookup"><span data-stu-id="d689b-239">True</span></span>                                                             |
| <span data-ttu-id="d689b-240">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d689b-240">Is Indexed</span></span>             | <span data-ttu-id="d689b-241">False</span><span class="sxs-lookup"><span data-stu-id="d689b-241">False</span></span>                                                            |
| <span data-ttu-id="d689b-242">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d689b-242">In Global Catalog</span></span>      | <span data-ttu-id="d689b-243">False</span><span class="sxs-lookup"><span data-stu-id="d689b-243">False</span></span>                                                            |
| <span data-ttu-id="d689b-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d689b-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="d689b-245">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d689b-245">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="d689b-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d689b-246">Range-Lower</span></span>            | <span data-ttu-id="d689b-247">0</span><span class="sxs-lookup"><span data-stu-id="d689b-247">0</span></span>                                                                |
| <span data-ttu-id="d689b-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d689b-248">Range-Upper</span></span>            | <span data-ttu-id="d689b-249">16</span><span class="sxs-lookup"><span data-stu-id="d689b-249">16</span></span>                                                               |
| <span data-ttu-id="d689b-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d689b-250">Search-Flags</span></span>           | <span data-ttu-id="d689b-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d689b-251">0x00000000</span></span>                                                       |
| <span data-ttu-id="d689b-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d689b-252">System-Flags</span></span>           | <span data-ttu-id="d689b-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d689b-253">0x00000010</span></span>                                                       |
| <span data-ttu-id="d689b-254">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d689b-254">Classes used in</span></span>        | [<span data-ttu-id="d689b-255">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="d689b-255">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d689b-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d689b-256">Windows Server 2012</span></span>



| <span data-ttu-id="d689b-257">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d689b-257">Entry</span></span> | <span data-ttu-id="d689b-258">Wert</span><span class="sxs-lookup"><span data-stu-id="d689b-258">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d689b-259">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d689b-259">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d689b-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d689b-260">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d689b-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="d689b-261">System-Only</span></span>            | <span data-ttu-id="d689b-262">False</span><span class="sxs-lookup"><span data-stu-id="d689b-262">False</span></span>                                                            |
| <span data-ttu-id="d689b-263">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d689b-263">Is-Single-Valued</span></span>       | <span data-ttu-id="d689b-264">Richtig</span><span class="sxs-lookup"><span data-stu-id="d689b-264">True</span></span>                                                             |
| <span data-ttu-id="d689b-265">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d689b-265">Is Indexed</span></span>             | <span data-ttu-id="d689b-266">False</span><span class="sxs-lookup"><span data-stu-id="d689b-266">False</span></span>                                                            |
| <span data-ttu-id="d689b-267">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d689b-267">In Global Catalog</span></span>      | <span data-ttu-id="d689b-268">False</span><span class="sxs-lookup"><span data-stu-id="d689b-268">False</span></span>                                                            |
| <span data-ttu-id="d689b-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d689b-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="d689b-270">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d689b-270">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="d689b-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d689b-271">Range-Lower</span></span>            | <span data-ttu-id="d689b-272">0</span><span class="sxs-lookup"><span data-stu-id="d689b-272">0</span></span>                                                                |
| <span data-ttu-id="d689b-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d689b-273">Range-Upper</span></span>            | <span data-ttu-id="d689b-274">16</span><span class="sxs-lookup"><span data-stu-id="d689b-274">16</span></span>                                                               |
| <span data-ttu-id="d689b-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d689b-275">Search-Flags</span></span>           | <span data-ttu-id="d689b-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d689b-276">0x00000000</span></span>                                                       |
| <span data-ttu-id="d689b-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d689b-277">System-Flags</span></span>           | <span data-ttu-id="d689b-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d689b-278">0x00000010</span></span>                                                       |
| <span data-ttu-id="d689b-279">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d689b-279">Classes used in</span></span>        | [<span data-ttu-id="d689b-280">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="d689b-280">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





