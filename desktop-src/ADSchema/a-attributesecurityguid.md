---
title: Attribute-Security-GUID-Attribut
description: Der GUID, der zum Anwenden von Sicherheits Anmelde Informationen auf einen Satz von Objekten verwendet werden soll.
ms.assetid: df4709ec-273d-4294-8094-f396c10c06e2
ms.tgt_platform: multiple
keywords:
- Attribut-Security-GUID-Attribut AD-Schema
- attributeSecurityGuid-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Attribute-Security-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b2ada7c6c806bec1c524b0408750144ca1fd8b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104213795"
---
# <a name="attribute-security-guid-attribute"></a><span data-ttu-id="6e630-105">Attribute-Security-GUID-Attribut</span><span class="sxs-lookup"><span data-stu-id="6e630-105">Attribute-Security-GUID attribute</span></span>

<span data-ttu-id="6e630-106">Der GUID, der zum Anwenden von Sicherheits Anmelde Informationen auf einen Satz von Objekten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e630-106">The GUID to be used to apply security credentials to a set of objects.</span></span>



| <span data-ttu-id="6e630-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6e630-107">Entry</span></span> | <span data-ttu-id="6e630-108">Wert</span><span class="sxs-lookup"><span data-stu-id="6e630-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="6e630-109">CN</span><span class="sxs-lookup"><span data-stu-id="6e630-109">CN</span></span>                | <span data-ttu-id="6e630-110">Attribute-Security-GUID</span><span class="sxs-lookup"><span data-stu-id="6e630-110">Attribute-Security-GUID</span></span>                               |
| <span data-ttu-id="6e630-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6e630-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6e630-112">attributeSecurityGUID</span><span class="sxs-lookup"><span data-stu-id="6e630-112">attributeSecurityGUID</span></span>                                 |
| <span data-ttu-id="6e630-113">Size</span><span class="sxs-lookup"><span data-stu-id="6e630-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="6e630-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="6e630-114">Update Privilege</span></span>  | <span data-ttu-id="6e630-115">Schema Administrator</span><span class="sxs-lookup"><span data-stu-id="6e630-115">Schema administrator</span></span>                                  |
| <span data-ttu-id="6e630-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="6e630-116">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="6e630-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6e630-117">Attribute-Id</span></span>      | <span data-ttu-id="6e630-118">1.2.840.113556.1.4.149</span><span class="sxs-lookup"><span data-stu-id="6e630-118">1.2.840.113556.1.4.149</span></span>                                |
| <span data-ttu-id="6e630-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6e630-119">System-Id-Guid</span></span>    | <span data-ttu-id="6e630-120">bf967924-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6e630-120">bf967924-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="6e630-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e630-121">Syntax</span></span>            | [<span data-ttu-id="6e630-122">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="6e630-122">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="6e630-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="6e630-123">Implementations</span></span>

-   [<span data-ttu-id="6e630-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6e630-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6e630-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6e630-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6e630-126">**Adam**</span><span class="sxs-lookup"><span data-stu-id="6e630-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6e630-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6e630-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6e630-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6e630-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6e630-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6e630-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6e630-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6e630-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6e630-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6e630-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6e630-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6e630-132">Entry</span></span> | <span data-ttu-id="6e630-133">Wert</span><span class="sxs-lookup"><span data-stu-id="6e630-133">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6e630-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6e630-134">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e630-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e630-135">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e630-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e630-136">System-Only</span></span>            | <span data-ttu-id="6e630-137">False</span><span class="sxs-lookup"><span data-stu-id="6e630-137">False</span></span>                                                    |
| <span data-ttu-id="6e630-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6e630-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6e630-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="6e630-139">True</span></span>                                                     |
| <span data-ttu-id="6e630-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6e630-140">Is Indexed</span></span>             | <span data-ttu-id="6e630-141">False</span><span class="sxs-lookup"><span data-stu-id="6e630-141">False</span></span>                                                    |
| <span data-ttu-id="6e630-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6e630-142">In Global Catalog</span></span>      | <span data-ttu-id="6e630-143">False</span><span class="sxs-lookup"><span data-stu-id="6e630-143">False</span></span>                                                    |
| <span data-ttu-id="6e630-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6e630-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e630-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6e630-145">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6e630-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e630-146">Range-Lower</span></span>            | <span data-ttu-id="6e630-147">16</span><span class="sxs-lookup"><span data-stu-id="6e630-147">16</span></span>                                                       |
| <span data-ttu-id="6e630-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e630-148">Range-Upper</span></span>            | <span data-ttu-id="6e630-149">16</span><span class="sxs-lookup"><span data-stu-id="6e630-149">16</span></span>                                                       |
| <span data-ttu-id="6e630-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e630-150">Search-Flags</span></span>           | <span data-ttu-id="6e630-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e630-151">0x00000000</span></span>                                               |
| <span data-ttu-id="6e630-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e630-152">System-Flags</span></span>           | <span data-ttu-id="6e630-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e630-153">0x00000010</span></span>                                               |
| <span data-ttu-id="6e630-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6e630-154">Classes used in</span></span>        | [<span data-ttu-id="6e630-155">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="6e630-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6e630-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6e630-156">Windows Server 2003</span></span>



| <span data-ttu-id="6e630-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6e630-157">Entry</span></span> | <span data-ttu-id="6e630-158">Wert</span><span class="sxs-lookup"><span data-stu-id="6e630-158">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6e630-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6e630-159">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e630-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e630-160">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e630-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e630-161">System-Only</span></span>            | <span data-ttu-id="6e630-162">False</span><span class="sxs-lookup"><span data-stu-id="6e630-162">False</span></span>                                                    |
| <span data-ttu-id="6e630-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6e630-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6e630-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="6e630-164">True</span></span>                                                     |
| <span data-ttu-id="6e630-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6e630-165">Is Indexed</span></span>             | <span data-ttu-id="6e630-166">False</span><span class="sxs-lookup"><span data-stu-id="6e630-166">False</span></span>                                                    |
| <span data-ttu-id="6e630-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6e630-167">In Global Catalog</span></span>      | <span data-ttu-id="6e630-168">False</span><span class="sxs-lookup"><span data-stu-id="6e630-168">False</span></span>                                                    |
| <span data-ttu-id="6e630-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6e630-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e630-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6e630-170">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6e630-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e630-171">Range-Lower</span></span>            | <span data-ttu-id="6e630-172">16</span><span class="sxs-lookup"><span data-stu-id="6e630-172">16</span></span>                                                       |
| <span data-ttu-id="6e630-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e630-173">Range-Upper</span></span>            | <span data-ttu-id="6e630-174">16</span><span class="sxs-lookup"><span data-stu-id="6e630-174">16</span></span>                                                       |
| <span data-ttu-id="6e630-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e630-175">Search-Flags</span></span>           | <span data-ttu-id="6e630-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e630-176">0x00000000</span></span>                                               |
| <span data-ttu-id="6e630-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e630-177">System-Flags</span></span>           | <span data-ttu-id="6e630-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e630-178">0x00000010</span></span>                                               |
| <span data-ttu-id="6e630-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6e630-179">Classes used in</span></span>        | [<span data-ttu-id="6e630-180">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="6e630-180">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6e630-181">Adam</span><span class="sxs-lookup"><span data-stu-id="6e630-181">ADAM</span></span>



| <span data-ttu-id="6e630-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6e630-182">Entry</span></span> | <span data-ttu-id="6e630-183">Wert</span><span class="sxs-lookup"><span data-stu-id="6e630-183">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6e630-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6e630-184">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e630-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e630-185">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e630-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e630-186">System-Only</span></span>            | <span data-ttu-id="6e630-187">False</span><span class="sxs-lookup"><span data-stu-id="6e630-187">False</span></span>                                                    |
| <span data-ttu-id="6e630-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6e630-188">Is-Single-Valued</span></span>       | <span data-ttu-id="6e630-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="6e630-189">True</span></span>                                                     |
| <span data-ttu-id="6e630-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6e630-190">Is Indexed</span></span>             | <span data-ttu-id="6e630-191">False</span><span class="sxs-lookup"><span data-stu-id="6e630-191">False</span></span>                                                    |
| <span data-ttu-id="6e630-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6e630-192">In Global Catalog</span></span>      | <span data-ttu-id="6e630-193">False</span><span class="sxs-lookup"><span data-stu-id="6e630-193">False</span></span>                                                    |
| <span data-ttu-id="6e630-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6e630-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e630-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6e630-195">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6e630-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e630-196">Range-Lower</span></span>            | <span data-ttu-id="6e630-197">16</span><span class="sxs-lookup"><span data-stu-id="6e630-197">16</span></span>                                                       |
| <span data-ttu-id="6e630-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e630-198">Range-Upper</span></span>            | <span data-ttu-id="6e630-199">16</span><span class="sxs-lookup"><span data-stu-id="6e630-199">16</span></span>                                                       |
| <span data-ttu-id="6e630-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e630-200">Search-Flags</span></span>           | <span data-ttu-id="6e630-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e630-201">0x00000000</span></span>                                               |
| <span data-ttu-id="6e630-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e630-202">System-Flags</span></span>           | <span data-ttu-id="6e630-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e630-203">0x00000010</span></span>                                               |
| <span data-ttu-id="6e630-204">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6e630-204">Classes used in</span></span>        | [<span data-ttu-id="6e630-205">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="6e630-205">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6e630-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6e630-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6e630-207">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6e630-207">Entry</span></span> | <span data-ttu-id="6e630-208">Wert</span><span class="sxs-lookup"><span data-stu-id="6e630-208">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6e630-209">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6e630-209">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e630-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e630-210">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e630-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e630-211">System-Only</span></span>            | <span data-ttu-id="6e630-212">False</span><span class="sxs-lookup"><span data-stu-id="6e630-212">False</span></span>                                                    |
| <span data-ttu-id="6e630-213">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6e630-213">Is-Single-Valued</span></span>       | <span data-ttu-id="6e630-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="6e630-214">True</span></span>                                                     |
| <span data-ttu-id="6e630-215">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6e630-215">Is Indexed</span></span>             | <span data-ttu-id="6e630-216">False</span><span class="sxs-lookup"><span data-stu-id="6e630-216">False</span></span>                                                    |
| <span data-ttu-id="6e630-217">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6e630-217">In Global Catalog</span></span>      | <span data-ttu-id="6e630-218">False</span><span class="sxs-lookup"><span data-stu-id="6e630-218">False</span></span>                                                    |
| <span data-ttu-id="6e630-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6e630-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e630-220">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6e630-220">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6e630-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e630-221">Range-Lower</span></span>            | <span data-ttu-id="6e630-222">16</span><span class="sxs-lookup"><span data-stu-id="6e630-222">16</span></span>                                                       |
| <span data-ttu-id="6e630-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e630-223">Range-Upper</span></span>            | <span data-ttu-id="6e630-224">16</span><span class="sxs-lookup"><span data-stu-id="6e630-224">16</span></span>                                                       |
| <span data-ttu-id="6e630-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e630-225">Search-Flags</span></span>           | <span data-ttu-id="6e630-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e630-226">0x00000000</span></span>                                               |
| <span data-ttu-id="6e630-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e630-227">System-Flags</span></span>           | <span data-ttu-id="6e630-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e630-228">0x00000010</span></span>                                               |
| <span data-ttu-id="6e630-229">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6e630-229">Classes used in</span></span>        | [<span data-ttu-id="6e630-230">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="6e630-230">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6e630-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e630-231">Windows Server 2008</span></span>



| <span data-ttu-id="6e630-232">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6e630-232">Entry</span></span> | <span data-ttu-id="6e630-233">Wert</span><span class="sxs-lookup"><span data-stu-id="6e630-233">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6e630-234">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6e630-234">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e630-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e630-235">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e630-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e630-236">System-Only</span></span>            | <span data-ttu-id="6e630-237">False</span><span class="sxs-lookup"><span data-stu-id="6e630-237">False</span></span>                                                    |
| <span data-ttu-id="6e630-238">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6e630-238">Is-Single-Valued</span></span>       | <span data-ttu-id="6e630-239">Richtig</span><span class="sxs-lookup"><span data-stu-id="6e630-239">True</span></span>                                                     |
| <span data-ttu-id="6e630-240">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6e630-240">Is Indexed</span></span>             | <span data-ttu-id="6e630-241">False</span><span class="sxs-lookup"><span data-stu-id="6e630-241">False</span></span>                                                    |
| <span data-ttu-id="6e630-242">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6e630-242">In Global Catalog</span></span>      | <span data-ttu-id="6e630-243">False</span><span class="sxs-lookup"><span data-stu-id="6e630-243">False</span></span>                                                    |
| <span data-ttu-id="6e630-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6e630-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e630-245">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6e630-245">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6e630-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e630-246">Range-Lower</span></span>            | <span data-ttu-id="6e630-247">16</span><span class="sxs-lookup"><span data-stu-id="6e630-247">16</span></span>                                                       |
| <span data-ttu-id="6e630-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e630-248">Range-Upper</span></span>            | <span data-ttu-id="6e630-249">16</span><span class="sxs-lookup"><span data-stu-id="6e630-249">16</span></span>                                                       |
| <span data-ttu-id="6e630-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e630-250">Search-Flags</span></span>           | <span data-ttu-id="6e630-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e630-251">0x00000000</span></span>                                               |
| <span data-ttu-id="6e630-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e630-252">System-Flags</span></span>           | <span data-ttu-id="6e630-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e630-253">0x00000010</span></span>                                               |
| <span data-ttu-id="6e630-254">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6e630-254">Classes used in</span></span>        | [<span data-ttu-id="6e630-255">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="6e630-255">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6e630-256">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6e630-256">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6e630-257">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6e630-257">Entry</span></span> | <span data-ttu-id="6e630-258">Wert</span><span class="sxs-lookup"><span data-stu-id="6e630-258">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6e630-259">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6e630-259">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e630-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e630-260">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e630-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e630-261">System-Only</span></span>            | <span data-ttu-id="6e630-262">False</span><span class="sxs-lookup"><span data-stu-id="6e630-262">False</span></span>                                                    |
| <span data-ttu-id="6e630-263">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6e630-263">Is-Single-Valued</span></span>       | <span data-ttu-id="6e630-264">Richtig</span><span class="sxs-lookup"><span data-stu-id="6e630-264">True</span></span>                                                     |
| <span data-ttu-id="6e630-265">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6e630-265">Is Indexed</span></span>             | <span data-ttu-id="6e630-266">False</span><span class="sxs-lookup"><span data-stu-id="6e630-266">False</span></span>                                                    |
| <span data-ttu-id="6e630-267">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6e630-267">In Global Catalog</span></span>      | <span data-ttu-id="6e630-268">False</span><span class="sxs-lookup"><span data-stu-id="6e630-268">False</span></span>                                                    |
| <span data-ttu-id="6e630-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6e630-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e630-270">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6e630-270">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6e630-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e630-271">Range-Lower</span></span>            | <span data-ttu-id="6e630-272">16</span><span class="sxs-lookup"><span data-stu-id="6e630-272">16</span></span>                                                       |
| <span data-ttu-id="6e630-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e630-273">Range-Upper</span></span>            | <span data-ttu-id="6e630-274">16</span><span class="sxs-lookup"><span data-stu-id="6e630-274">16</span></span>                                                       |
| <span data-ttu-id="6e630-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e630-275">Search-Flags</span></span>           | <span data-ttu-id="6e630-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e630-276">0x00000000</span></span>                                               |
| <span data-ttu-id="6e630-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e630-277">System-Flags</span></span>           | <span data-ttu-id="6e630-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e630-278">0x00000010</span></span>                                               |
| <span data-ttu-id="6e630-279">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6e630-279">Classes used in</span></span>        | [<span data-ttu-id="6e630-280">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="6e630-280">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6e630-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6e630-281">Windows Server 2012</span></span>



| <span data-ttu-id="6e630-282">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6e630-282">Entry</span></span> | <span data-ttu-id="6e630-283">Wert</span><span class="sxs-lookup"><span data-stu-id="6e630-283">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="6e630-284">Link-ID</span><span class="sxs-lookup"><span data-stu-id="6e630-284">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e630-285">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e630-285">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="6e630-286">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e630-286">System-Only</span></span>            | <span data-ttu-id="6e630-287">False</span><span class="sxs-lookup"><span data-stu-id="6e630-287">False</span></span>                                                    |
| <span data-ttu-id="6e630-288">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="6e630-288">Is-Single-Valued</span></span>       | <span data-ttu-id="6e630-289">Richtig</span><span class="sxs-lookup"><span data-stu-id="6e630-289">True</span></span>                                                     |
| <span data-ttu-id="6e630-290">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="6e630-290">Is Indexed</span></span>             | <span data-ttu-id="6e630-291">False</span><span class="sxs-lookup"><span data-stu-id="6e630-291">False</span></span>                                                    |
| <span data-ttu-id="6e630-292">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="6e630-292">In Global Catalog</span></span>      | <span data-ttu-id="6e630-293">False</span><span class="sxs-lookup"><span data-stu-id="6e630-293">False</span></span>                                                    |
| <span data-ttu-id="6e630-294">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6e630-294">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e630-295">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="6e630-295">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="6e630-296">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e630-296">Range-Lower</span></span>            | <span data-ttu-id="6e630-297">16</span><span class="sxs-lookup"><span data-stu-id="6e630-297">16</span></span>                                                       |
| <span data-ttu-id="6e630-298">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e630-298">Range-Upper</span></span>            | <span data-ttu-id="6e630-299">16</span><span class="sxs-lookup"><span data-stu-id="6e630-299">16</span></span>                                                       |
| <span data-ttu-id="6e630-300">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e630-300">Search-Flags</span></span>           | <span data-ttu-id="6e630-301">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e630-301">0x00000000</span></span>                                               |
| <span data-ttu-id="6e630-302">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e630-302">System-Flags</span></span>           | <span data-ttu-id="6e630-303">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e630-303">0x00000010</span></span>                                               |
| <span data-ttu-id="6e630-304">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="6e630-304">Classes used in</span></span>        | [<span data-ttu-id="6e630-305">**Attribut-Schema**</span><span class="sxs-lookup"><span data-stu-id="6e630-305">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 





