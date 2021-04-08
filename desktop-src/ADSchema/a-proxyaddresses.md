---
title: Proxy-Addresses-Attribut
description: Eine Proxy Adresse ist die Adresse, mit der ein Microsoft Exchange Server-Empfänger Objekt in einem fremden e-Mail-System erkannt wird. Proxy Adressen sind für alle Empfänger Objekte erforderlich, z. b. benutzerdefinierte Empfänger und Verteilerlisten.
ms.assetid: 7bb299d8-e67a-4062-91a3-b579fd71d5c9
ms.tgt_platform: multiple
keywords:
- AD-Schema für Proxy-Addresses-Attribut
- Proxyadressen-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Proxy-Addresses
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03542cef9bca48dbba1585e3837056b53673f34
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859771"
---
# <a name="proxy-addresses-attribute"></a><span data-ttu-id="dfdbb-106">Proxy-Addresses-Attribut</span><span class="sxs-lookup"><span data-stu-id="dfdbb-106">Proxy-Addresses attribute</span></span>

<span data-ttu-id="dfdbb-107">Eine Proxy Adresse ist die Adresse, mit der ein Microsoft Exchange Server-Empfänger Objekt in einem fremden e-Mail-System erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="dfdbb-107">A proxy address is the address by which a Microsoft Exchange Server recipient object is recognized in a foreign mail system.</span></span> <span data-ttu-id="dfdbb-108">Proxy Adressen sind für alle Empfänger Objekte erforderlich, z. b. benutzerdefinierte Empfänger und Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="dfdbb-108">Proxy addresses are required for all recipient objects, such as custom recipients and distribution lists.</span></span>



| <span data-ttu-id="dfdbb-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfdbb-109">Entry</span></span> | <span data-ttu-id="dfdbb-110">Wert</span><span class="sxs-lookup"><span data-stu-id="dfdbb-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfdbb-111">CN</span><span class="sxs-lookup"><span data-stu-id="dfdbb-111">CN</span></span>                | <span data-ttu-id="dfdbb-112">Proxy-Addresses</span><span class="sxs-lookup"><span data-stu-id="dfdbb-112">Proxy-Addresses</span></span>                                                                                      |
| <span data-ttu-id="dfdbb-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="dfdbb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="dfdbb-114">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="dfdbb-114">proxyAddresses</span></span>                                                                                       |
| <span data-ttu-id="dfdbb-115">Size</span><span class="sxs-lookup"><span data-stu-id="dfdbb-115">Size</span></span>              | \-                                                                                                   |
| <span data-ttu-id="dfdbb-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="dfdbb-116">Update Privilege</span></span>  | <span data-ttu-id="dfdbb-117">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dfdbb-117">This value is set by the system.</span></span>                                                                     |
| <span data-ttu-id="dfdbb-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="dfdbb-118">Update Frequency</span></span>  | <span data-ttu-id="dfdbb-119">Wird durch eine DLL erstellt, die bei der Installation des Adress Typs mit dem Address-Type Directory-Objekt bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="dfdbb-119">Created by a DLL provided with the Address-Type directory object when the address type is installed.</span></span> |
| <span data-ttu-id="dfdbb-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dfdbb-120">Attribute-Id</span></span>      | <span data-ttu-id="dfdbb-121">1.2.840.113556.1.2.210</span><span class="sxs-lookup"><span data-stu-id="dfdbb-121">1.2.840.113556.1.2.210</span></span>                                                                               |
| <span data-ttu-id="dfdbb-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dfdbb-122">System-Id-Guid</span></span>    | <span data-ttu-id="dfdbb-123">bf967a06-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="dfdbb-123">bf967a06-0de6-11d0-a285-00aa003049e2</span></span>                                                                 |
| <span data-ttu-id="dfdbb-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfdbb-124">Syntax</span></span>            | [<span data-ttu-id="dfdbb-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="dfdbb-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                                          |



## <a name="implementations"></a><span data-ttu-id="dfdbb-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="dfdbb-126">Implementations</span></span>

-   [<span data-ttu-id="dfdbb-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dfdbb-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dfdbb-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dfdbb-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dfdbb-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="dfdbb-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="dfdbb-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dfdbb-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dfdbb-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dfdbb-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dfdbb-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dfdbb-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dfdbb-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dfdbb-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dfdbb-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dfdbb-134">Windows 2000 Server</span></span>



| <span data-ttu-id="dfdbb-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfdbb-135">Entry</span></span> | <span data-ttu-id="dfdbb-136">Wert</span><span class="sxs-lookup"><span data-stu-id="dfdbb-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dfdbb-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dfdbb-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dfdbb-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfdbb-138">MAPI-Id</span></span>                | <span data-ttu-id="dfdbb-139">0x800f</span><span class="sxs-lookup"><span data-stu-id="dfdbb-139">0x800F</span></span>                          |
| <span data-ttu-id="dfdbb-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfdbb-140">System-Only</span></span>            | <span data-ttu-id="dfdbb-141">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-141">False</span></span>                           |
| <span data-ttu-id="dfdbb-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dfdbb-142">Is-Single-Valued</span></span>       | <span data-ttu-id="dfdbb-143">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-143">False</span></span>                           |
| <span data-ttu-id="dfdbb-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dfdbb-144">Is Indexed</span></span>             | <span data-ttu-id="dfdbb-145">Richtig</span><span class="sxs-lookup"><span data-stu-id="dfdbb-145">True</span></span>                            |
| <span data-ttu-id="dfdbb-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dfdbb-146">In Global Catalog</span></span>      | <span data-ttu-id="dfdbb-147">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-147">False</span></span>                           |
| <span data-ttu-id="dfdbb-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfdbb-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfdbb-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dfdbb-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dfdbb-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfdbb-150">Range-Lower</span></span>            | <span data-ttu-id="dfdbb-151">1</span><span class="sxs-lookup"><span data-stu-id="dfdbb-151">1</span></span>                               |
| <span data-ttu-id="dfdbb-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfdbb-152">Range-Upper</span></span>            | <span data-ttu-id="dfdbb-153">1123</span><span class="sxs-lookup"><span data-stu-id="dfdbb-153">1123</span></span>                            |
| <span data-ttu-id="dfdbb-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfdbb-154">Search-Flags</span></span>           | <span data-ttu-id="dfdbb-155">0x00000005</span><span class="sxs-lookup"><span data-stu-id="dfdbb-155">0x00000005</span></span>                      |
| <span data-ttu-id="dfdbb-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfdbb-156">System-Flags</span></span>           | <span data-ttu-id="dfdbb-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfdbb-157">0x00000010</span></span>                      |
| <span data-ttu-id="dfdbb-158">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dfdbb-158">Classes used in</span></span>        | [<span data-ttu-id="dfdbb-159">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="dfdbb-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dfdbb-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dfdbb-160">Windows Server 2003</span></span>



| <span data-ttu-id="dfdbb-161">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfdbb-161">Entry</span></span> | <span data-ttu-id="dfdbb-162">Wert</span><span class="sxs-lookup"><span data-stu-id="dfdbb-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dfdbb-163">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dfdbb-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dfdbb-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfdbb-164">MAPI-Id</span></span>                | <span data-ttu-id="dfdbb-165">0x800f</span><span class="sxs-lookup"><span data-stu-id="dfdbb-165">0x800F</span></span>                          |
| <span data-ttu-id="dfdbb-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfdbb-166">System-Only</span></span>            | <span data-ttu-id="dfdbb-167">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-167">False</span></span>                           |
| <span data-ttu-id="dfdbb-168">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dfdbb-168">Is-Single-Valued</span></span>       | <span data-ttu-id="dfdbb-169">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-169">False</span></span>                           |
| <span data-ttu-id="dfdbb-170">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dfdbb-170">Is Indexed</span></span>             | <span data-ttu-id="dfdbb-171">Richtig</span><span class="sxs-lookup"><span data-stu-id="dfdbb-171">True</span></span>                            |
| <span data-ttu-id="dfdbb-172">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dfdbb-172">In Global Catalog</span></span>      | <span data-ttu-id="dfdbb-173">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-173">False</span></span>                           |
| <span data-ttu-id="dfdbb-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfdbb-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfdbb-175">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dfdbb-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dfdbb-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfdbb-176">Range-Lower</span></span>            | <span data-ttu-id="dfdbb-177">1</span><span class="sxs-lookup"><span data-stu-id="dfdbb-177">1</span></span>                               |
| <span data-ttu-id="dfdbb-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfdbb-178">Range-Upper</span></span>            | <span data-ttu-id="dfdbb-179">1123</span><span class="sxs-lookup"><span data-stu-id="dfdbb-179">1123</span></span>                            |
| <span data-ttu-id="dfdbb-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfdbb-180">Search-Flags</span></span>           | <span data-ttu-id="dfdbb-181">0x00000005</span><span class="sxs-lookup"><span data-stu-id="dfdbb-181">0x00000005</span></span>                      |
| <span data-ttu-id="dfdbb-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfdbb-182">System-Flags</span></span>           | <span data-ttu-id="dfdbb-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfdbb-183">0x00000010</span></span>                      |
| <span data-ttu-id="dfdbb-184">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dfdbb-184">Classes used in</span></span>        | [<span data-ttu-id="dfdbb-185">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="dfdbb-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="dfdbb-186">Adam</span><span class="sxs-lookup"><span data-stu-id="dfdbb-186">ADAM</span></span>



| <span data-ttu-id="dfdbb-187">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfdbb-187">Entry</span></span> | <span data-ttu-id="dfdbb-188">Wert</span><span class="sxs-lookup"><span data-stu-id="dfdbb-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dfdbb-189">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dfdbb-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dfdbb-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfdbb-190">MAPI-Id</span></span>                | <span data-ttu-id="dfdbb-191">0x800f</span><span class="sxs-lookup"><span data-stu-id="dfdbb-191">0x800F</span></span>                          |
| <span data-ttu-id="dfdbb-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfdbb-192">System-Only</span></span>            | <span data-ttu-id="dfdbb-193">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-193">False</span></span>                           |
| <span data-ttu-id="dfdbb-194">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dfdbb-194">Is-Single-Valued</span></span>       | <span data-ttu-id="dfdbb-195">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-195">False</span></span>                           |
| <span data-ttu-id="dfdbb-196">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dfdbb-196">Is Indexed</span></span>             | <span data-ttu-id="dfdbb-197">Richtig</span><span class="sxs-lookup"><span data-stu-id="dfdbb-197">True</span></span>                            |
| <span data-ttu-id="dfdbb-198">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dfdbb-198">In Global Catalog</span></span>      | <span data-ttu-id="dfdbb-199">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-199">False</span></span>                           |
| <span data-ttu-id="dfdbb-200">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfdbb-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfdbb-201">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dfdbb-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dfdbb-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfdbb-202">Range-Lower</span></span>            | <span data-ttu-id="dfdbb-203">1</span><span class="sxs-lookup"><span data-stu-id="dfdbb-203">1</span></span>                               |
| <span data-ttu-id="dfdbb-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfdbb-204">Range-Upper</span></span>            | <span data-ttu-id="dfdbb-205">1123</span><span class="sxs-lookup"><span data-stu-id="dfdbb-205">1123</span></span>                            |
| <span data-ttu-id="dfdbb-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfdbb-206">Search-Flags</span></span>           | <span data-ttu-id="dfdbb-207">0x00000005</span><span class="sxs-lookup"><span data-stu-id="dfdbb-207">0x00000005</span></span>                      |
| <span data-ttu-id="dfdbb-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfdbb-208">System-Flags</span></span>           | <span data-ttu-id="dfdbb-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfdbb-209">0x00000010</span></span>                      |
| <span data-ttu-id="dfdbb-210">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dfdbb-210">Classes used in</span></span>        | [<span data-ttu-id="dfdbb-211">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="dfdbb-211">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dfdbb-212">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dfdbb-212">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dfdbb-213">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfdbb-213">Entry</span></span> | <span data-ttu-id="dfdbb-214">Wert</span><span class="sxs-lookup"><span data-stu-id="dfdbb-214">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dfdbb-215">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dfdbb-215">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dfdbb-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfdbb-216">MAPI-Id</span></span>                | <span data-ttu-id="dfdbb-217">0x800f</span><span class="sxs-lookup"><span data-stu-id="dfdbb-217">0x800F</span></span>                          |
| <span data-ttu-id="dfdbb-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfdbb-218">System-Only</span></span>            | <span data-ttu-id="dfdbb-219">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-219">False</span></span>                           |
| <span data-ttu-id="dfdbb-220">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dfdbb-220">Is-Single-Valued</span></span>       | <span data-ttu-id="dfdbb-221">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-221">False</span></span>                           |
| <span data-ttu-id="dfdbb-222">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dfdbb-222">Is Indexed</span></span>             | <span data-ttu-id="dfdbb-223">Richtig</span><span class="sxs-lookup"><span data-stu-id="dfdbb-223">True</span></span>                            |
| <span data-ttu-id="dfdbb-224">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dfdbb-224">In Global Catalog</span></span>      | <span data-ttu-id="dfdbb-225">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-225">False</span></span>                           |
| <span data-ttu-id="dfdbb-226">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfdbb-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfdbb-227">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dfdbb-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dfdbb-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfdbb-228">Range-Lower</span></span>            | <span data-ttu-id="dfdbb-229">1</span><span class="sxs-lookup"><span data-stu-id="dfdbb-229">1</span></span>                               |
| <span data-ttu-id="dfdbb-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfdbb-230">Range-Upper</span></span>            | <span data-ttu-id="dfdbb-231">1123</span><span class="sxs-lookup"><span data-stu-id="dfdbb-231">1123</span></span>                            |
| <span data-ttu-id="dfdbb-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfdbb-232">Search-Flags</span></span>           | <span data-ttu-id="dfdbb-233">0x00000005</span><span class="sxs-lookup"><span data-stu-id="dfdbb-233">0x00000005</span></span>                      |
| <span data-ttu-id="dfdbb-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfdbb-234">System-Flags</span></span>           | <span data-ttu-id="dfdbb-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfdbb-235">0x00000010</span></span>                      |
| <span data-ttu-id="dfdbb-236">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dfdbb-236">Classes used in</span></span>        | [<span data-ttu-id="dfdbb-237">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="dfdbb-237">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dfdbb-238">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfdbb-238">Windows Server 2008</span></span>



| <span data-ttu-id="dfdbb-239">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfdbb-239">Entry</span></span> | <span data-ttu-id="dfdbb-240">Wert</span><span class="sxs-lookup"><span data-stu-id="dfdbb-240">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dfdbb-241">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dfdbb-241">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dfdbb-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfdbb-242">MAPI-Id</span></span>                | <span data-ttu-id="dfdbb-243">0x800f</span><span class="sxs-lookup"><span data-stu-id="dfdbb-243">0x800F</span></span>                          |
| <span data-ttu-id="dfdbb-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfdbb-244">System-Only</span></span>            | <span data-ttu-id="dfdbb-245">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-245">False</span></span>                           |
| <span data-ttu-id="dfdbb-246">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dfdbb-246">Is-Single-Valued</span></span>       | <span data-ttu-id="dfdbb-247">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-247">False</span></span>                           |
| <span data-ttu-id="dfdbb-248">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dfdbb-248">Is Indexed</span></span>             | <span data-ttu-id="dfdbb-249">Richtig</span><span class="sxs-lookup"><span data-stu-id="dfdbb-249">True</span></span>                            |
| <span data-ttu-id="dfdbb-250">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dfdbb-250">In Global Catalog</span></span>      | <span data-ttu-id="dfdbb-251">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-251">False</span></span>                           |
| <span data-ttu-id="dfdbb-252">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfdbb-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfdbb-253">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dfdbb-253">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dfdbb-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfdbb-254">Range-Lower</span></span>            | <span data-ttu-id="dfdbb-255">1</span><span class="sxs-lookup"><span data-stu-id="dfdbb-255">1</span></span>                               |
| <span data-ttu-id="dfdbb-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfdbb-256">Range-Upper</span></span>            | <span data-ttu-id="dfdbb-257">1123</span><span class="sxs-lookup"><span data-stu-id="dfdbb-257">1123</span></span>                            |
| <span data-ttu-id="dfdbb-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfdbb-258">Search-Flags</span></span>           | <span data-ttu-id="dfdbb-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="dfdbb-259">0x00000005</span></span>                      |
| <span data-ttu-id="dfdbb-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfdbb-260">System-Flags</span></span>           | <span data-ttu-id="dfdbb-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfdbb-261">0x00000010</span></span>                      |
| <span data-ttu-id="dfdbb-262">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dfdbb-262">Classes used in</span></span>        | [<span data-ttu-id="dfdbb-263">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="dfdbb-263">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dfdbb-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dfdbb-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dfdbb-265">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfdbb-265">Entry</span></span> | <span data-ttu-id="dfdbb-266">Wert</span><span class="sxs-lookup"><span data-stu-id="dfdbb-266">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dfdbb-267">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dfdbb-267">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dfdbb-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfdbb-268">MAPI-Id</span></span>                | <span data-ttu-id="dfdbb-269">0x800f</span><span class="sxs-lookup"><span data-stu-id="dfdbb-269">0x800F</span></span>                          |
| <span data-ttu-id="dfdbb-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfdbb-270">System-Only</span></span>            | <span data-ttu-id="dfdbb-271">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-271">False</span></span>                           |
| <span data-ttu-id="dfdbb-272">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dfdbb-272">Is-Single-Valued</span></span>       | <span data-ttu-id="dfdbb-273">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-273">False</span></span>                           |
| <span data-ttu-id="dfdbb-274">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dfdbb-274">Is Indexed</span></span>             | <span data-ttu-id="dfdbb-275">Richtig</span><span class="sxs-lookup"><span data-stu-id="dfdbb-275">True</span></span>                            |
| <span data-ttu-id="dfdbb-276">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dfdbb-276">In Global Catalog</span></span>      | <span data-ttu-id="dfdbb-277">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-277">False</span></span>                           |
| <span data-ttu-id="dfdbb-278">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfdbb-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfdbb-279">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dfdbb-279">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dfdbb-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfdbb-280">Range-Lower</span></span>            | <span data-ttu-id="dfdbb-281">1</span><span class="sxs-lookup"><span data-stu-id="dfdbb-281">1</span></span>                               |
| <span data-ttu-id="dfdbb-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfdbb-282">Range-Upper</span></span>            | <span data-ttu-id="dfdbb-283">1123</span><span class="sxs-lookup"><span data-stu-id="dfdbb-283">1123</span></span>                            |
| <span data-ttu-id="dfdbb-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfdbb-284">Search-Flags</span></span>           | <span data-ttu-id="dfdbb-285">0x00000005</span><span class="sxs-lookup"><span data-stu-id="dfdbb-285">0x00000005</span></span>                      |
| <span data-ttu-id="dfdbb-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfdbb-286">System-Flags</span></span>           | <span data-ttu-id="dfdbb-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfdbb-287">0x00000010</span></span>                      |
| <span data-ttu-id="dfdbb-288">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dfdbb-288">Classes used in</span></span>        | [<span data-ttu-id="dfdbb-289">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="dfdbb-289">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dfdbb-290">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dfdbb-290">Windows Server 2012</span></span>



| <span data-ttu-id="dfdbb-291">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfdbb-291">Entry</span></span> | <span data-ttu-id="dfdbb-292">Wert</span><span class="sxs-lookup"><span data-stu-id="dfdbb-292">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dfdbb-293">Link-ID</span><span class="sxs-lookup"><span data-stu-id="dfdbb-293">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dfdbb-294">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfdbb-294">MAPI-Id</span></span>                | <span data-ttu-id="dfdbb-295">0x800f</span><span class="sxs-lookup"><span data-stu-id="dfdbb-295">0x800F</span></span>                          |
| <span data-ttu-id="dfdbb-296">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfdbb-296">System-Only</span></span>            | <span data-ttu-id="dfdbb-297">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-297">False</span></span>                           |
| <span data-ttu-id="dfdbb-298">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="dfdbb-298">Is-Single-Valued</span></span>       | <span data-ttu-id="dfdbb-299">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-299">False</span></span>                           |
| <span data-ttu-id="dfdbb-300">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="dfdbb-300">Is Indexed</span></span>             | <span data-ttu-id="dfdbb-301">Richtig</span><span class="sxs-lookup"><span data-stu-id="dfdbb-301">True</span></span>                            |
| <span data-ttu-id="dfdbb-302">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="dfdbb-302">In Global Catalog</span></span>      | <span data-ttu-id="dfdbb-303">False</span><span class="sxs-lookup"><span data-stu-id="dfdbb-303">False</span></span>                           |
| <span data-ttu-id="dfdbb-304">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfdbb-304">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfdbb-305">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="dfdbb-305">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dfdbb-306">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfdbb-306">Range-Lower</span></span>            | <span data-ttu-id="dfdbb-307">1</span><span class="sxs-lookup"><span data-stu-id="dfdbb-307">1</span></span>                               |
| <span data-ttu-id="dfdbb-308">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfdbb-308">Range-Upper</span></span>            | <span data-ttu-id="dfdbb-309">1123</span><span class="sxs-lookup"><span data-stu-id="dfdbb-309">1123</span></span>                            |
| <span data-ttu-id="dfdbb-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfdbb-310">Search-Flags</span></span>           | <span data-ttu-id="dfdbb-311">0x00000005</span><span class="sxs-lookup"><span data-stu-id="dfdbb-311">0x00000005</span></span>                      |
| <span data-ttu-id="dfdbb-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfdbb-312">System-Flags</span></span>           | <span data-ttu-id="dfdbb-313">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfdbb-313">0x00000010</span></span>                      |
| <span data-ttu-id="dfdbb-314">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="dfdbb-314">Classes used in</span></span>        | [<span data-ttu-id="dfdbb-315">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="dfdbb-315">**Top**</span></span>](c-top.md)<br/> |



 

 





