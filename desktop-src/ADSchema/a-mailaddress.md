---
title: SMTP-Mail-address-Attribut
description: Generisches Mail Adress Attribut. Wird im Feld als optionales Attribut von Server Objekten verwendet, wo es von e-Mail-basierter DS-Replikation genutzt wird (sofern die Computer so konfiguriert sind).
ms.assetid: 54fd710c-d140-4d46-9db3-0c72fb5fb08c
ms.tgt_platform: multiple
keywords:
- AD-Schema für SMTP-e-Mail-Adress Attribut
- MailAddress-Attribut AD-Schema
topic_type:
- apiref
api_name:
- SMTP-Mail-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1828c59af346ab5a5741aaa03358b711484089
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107228"
---
# <a name="smtp-mail-address-attribute"></a><span data-ttu-id="56a5a-106">SMTP-Mail-address-Attribut</span><span class="sxs-lookup"><span data-stu-id="56a5a-106">SMTP-Mail-Address attribute</span></span>

<span data-ttu-id="56a5a-107">Generisches Mail Adress Attribut.</span><span class="sxs-lookup"><span data-stu-id="56a5a-107">Generic mail address attribute.</span></span> <span data-ttu-id="56a5a-108">Wird im Feld als optionales Attribut von Server Objekten verwendet, wo es von e-Mail-basierter DS-Replikation genutzt wird (sofern die Computer so konfiguriert sind).</span><span class="sxs-lookup"><span data-stu-id="56a5a-108">Used in the box as an optional attribute of server objects, where it is consumed by mail-based DS replication (if the computers are so configured).</span></span>



| <span data-ttu-id="56a5a-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56a5a-109">Entry</span></span> | <span data-ttu-id="56a5a-110">Wert</span><span class="sxs-lookup"><span data-stu-id="56a5a-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="56a5a-111">CN</span><span class="sxs-lookup"><span data-stu-id="56a5a-111">CN</span></span>                | <span data-ttu-id="56a5a-112">SMTP-e-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="56a5a-112">SMTP-Mail-Address</span></span>                           |
| <span data-ttu-id="56a5a-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="56a5a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="56a5a-114">mailAddress</span><span class="sxs-lookup"><span data-stu-id="56a5a-114">mailAddress</span></span>                                 |
| <span data-ttu-id="56a5a-115">Size</span><span class="sxs-lookup"><span data-stu-id="56a5a-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="56a5a-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="56a5a-116">Update Privilege</span></span>  | <span data-ttu-id="56a5a-117">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="56a5a-117">Domain administrator</span></span>                        |
| <span data-ttu-id="56a5a-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="56a5a-118">Update Frequency</span></span>  | <span data-ttu-id="56a5a-119">Fast nie</span><span class="sxs-lookup"><span data-stu-id="56a5a-119">Almost never</span></span>                                |
| <span data-ttu-id="56a5a-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="56a5a-120">Attribute-Id</span></span>      | <span data-ttu-id="56a5a-121">1.2.840.113556.1.4.786</span><span class="sxs-lookup"><span data-stu-id="56a5a-121">1.2.840.113556.1.4.786</span></span>                      |
| <span data-ttu-id="56a5a-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="56a5a-122">System-Id-Guid</span></span>    | <span data-ttu-id="56a5a-123">26d9736b-6070-11d1-a9c6-0000 C1</span><span class="sxs-lookup"><span data-stu-id="56a5a-123">26d9736f-6070-11d1-a9c6-0000f80367c1</span></span>        |
| <span data-ttu-id="56a5a-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="56a5a-124">Syntax</span></span>            | [<span data-ttu-id="56a5a-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="56a5a-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="56a5a-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="56a5a-126">Implementations</span></span>

-   [<span data-ttu-id="56a5a-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="56a5a-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="56a5a-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="56a5a-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="56a5a-129">**Adam**</span><span class="sxs-lookup"><span data-stu-id="56a5a-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="56a5a-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="56a5a-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="56a5a-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="56a5a-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="56a5a-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="56a5a-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="56a5a-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="56a5a-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="56a5a-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="56a5a-134">Windows 2000 Server</span></span>



| <span data-ttu-id="56a5a-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56a5a-135">Entry</span></span> | <span data-ttu-id="56a5a-136">Wert</span><span class="sxs-lookup"><span data-stu-id="56a5a-136">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="56a5a-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="56a5a-137">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="56a5a-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56a5a-138">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="56a5a-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="56a5a-139">System-Only</span></span>            | <span data-ttu-id="56a5a-140">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-140">False</span></span>                                 |
| <span data-ttu-id="56a5a-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="56a5a-141">Is-Single-Valued</span></span>       | <span data-ttu-id="56a5a-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="56a5a-142">True</span></span>                                  |
| <span data-ttu-id="56a5a-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="56a5a-143">Is Indexed</span></span>             | <span data-ttu-id="56a5a-144">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-144">False</span></span>                                 |
| <span data-ttu-id="56a5a-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="56a5a-145">In Global Catalog</span></span>      | <span data-ttu-id="56a5a-146">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-146">False</span></span>                                 |
| <span data-ttu-id="56a5a-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56a5a-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="56a5a-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="56a5a-148">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="56a5a-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56a5a-149">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="56a5a-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56a5a-150">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="56a5a-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56a5a-151">Search-Flags</span></span>           | <span data-ttu-id="56a5a-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56a5a-152">0x00000000</span></span>                            |
| <span data-ttu-id="56a5a-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56a5a-153">System-Flags</span></span>           | <span data-ttu-id="56a5a-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56a5a-154">0x00000010</span></span>                            |
| <span data-ttu-id="56a5a-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="56a5a-155">Classes used in</span></span>        | [<span data-ttu-id="56a5a-156">**Servers**</span><span class="sxs-lookup"><span data-stu-id="56a5a-156">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="56a5a-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="56a5a-157">Windows Server 2003</span></span>



| <span data-ttu-id="56a5a-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56a5a-158">Entry</span></span> | <span data-ttu-id="56a5a-159">Wert</span><span class="sxs-lookup"><span data-stu-id="56a5a-159">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="56a5a-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="56a5a-160">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="56a5a-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56a5a-161">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="56a5a-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="56a5a-162">System-Only</span></span>            | <span data-ttu-id="56a5a-163">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-163">False</span></span>                                 |
| <span data-ttu-id="56a5a-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="56a5a-164">Is-Single-Valued</span></span>       | <span data-ttu-id="56a5a-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="56a5a-165">True</span></span>                                  |
| <span data-ttu-id="56a5a-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="56a5a-166">Is Indexed</span></span>             | <span data-ttu-id="56a5a-167">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-167">False</span></span>                                 |
| <span data-ttu-id="56a5a-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="56a5a-168">In Global Catalog</span></span>      | <span data-ttu-id="56a5a-169">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-169">False</span></span>                                 |
| <span data-ttu-id="56a5a-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56a5a-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="56a5a-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="56a5a-171">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="56a5a-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56a5a-172">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="56a5a-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56a5a-173">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="56a5a-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56a5a-174">Search-Flags</span></span>           | <span data-ttu-id="56a5a-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56a5a-175">0x00000000</span></span>                            |
| <span data-ttu-id="56a5a-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56a5a-176">System-Flags</span></span>           | <span data-ttu-id="56a5a-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56a5a-177">0x00000010</span></span>                            |
| <span data-ttu-id="56a5a-178">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="56a5a-178">Classes used in</span></span>        | [<span data-ttu-id="56a5a-179">**Servers**</span><span class="sxs-lookup"><span data-stu-id="56a5a-179">**Server**</span></span>](c-server.md)<br/> |



## <a name="adam"></a><span data-ttu-id="56a5a-180">Adam</span><span class="sxs-lookup"><span data-stu-id="56a5a-180">ADAM</span></span>



| <span data-ttu-id="56a5a-181">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56a5a-181">Entry</span></span> | <span data-ttu-id="56a5a-182">Wert</span><span class="sxs-lookup"><span data-stu-id="56a5a-182">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="56a5a-183">Link-ID</span><span class="sxs-lookup"><span data-stu-id="56a5a-183">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="56a5a-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56a5a-184">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="56a5a-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="56a5a-185">System-Only</span></span>            | <span data-ttu-id="56a5a-186">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-186">False</span></span>                                 |
| <span data-ttu-id="56a5a-187">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="56a5a-187">Is-Single-Valued</span></span>       | <span data-ttu-id="56a5a-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="56a5a-188">True</span></span>                                  |
| <span data-ttu-id="56a5a-189">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="56a5a-189">Is Indexed</span></span>             | <span data-ttu-id="56a5a-190">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-190">False</span></span>                                 |
| <span data-ttu-id="56a5a-191">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="56a5a-191">In Global Catalog</span></span>      | <span data-ttu-id="56a5a-192">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-192">False</span></span>                                 |
| <span data-ttu-id="56a5a-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56a5a-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="56a5a-194">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="56a5a-194">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="56a5a-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56a5a-195">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="56a5a-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56a5a-196">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="56a5a-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56a5a-197">Search-Flags</span></span>           | <span data-ttu-id="56a5a-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56a5a-198">0x00000000</span></span>                            |
| <span data-ttu-id="56a5a-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56a5a-199">System-Flags</span></span>           | <span data-ttu-id="56a5a-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56a5a-200">0x00000010</span></span>                            |
| <span data-ttu-id="56a5a-201">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="56a5a-201">Classes used in</span></span>        | [<span data-ttu-id="56a5a-202">**Servers**</span><span class="sxs-lookup"><span data-stu-id="56a5a-202">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="56a5a-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="56a5a-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="56a5a-204">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56a5a-204">Entry</span></span> | <span data-ttu-id="56a5a-205">Wert</span><span class="sxs-lookup"><span data-stu-id="56a5a-205">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="56a5a-206">Link-ID</span><span class="sxs-lookup"><span data-stu-id="56a5a-206">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="56a5a-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56a5a-207">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="56a5a-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="56a5a-208">System-Only</span></span>            | <span data-ttu-id="56a5a-209">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-209">False</span></span>                                 |
| <span data-ttu-id="56a5a-210">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="56a5a-210">Is-Single-Valued</span></span>       | <span data-ttu-id="56a5a-211">Richtig</span><span class="sxs-lookup"><span data-stu-id="56a5a-211">True</span></span>                                  |
| <span data-ttu-id="56a5a-212">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="56a5a-212">Is Indexed</span></span>             | <span data-ttu-id="56a5a-213">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-213">False</span></span>                                 |
| <span data-ttu-id="56a5a-214">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="56a5a-214">In Global Catalog</span></span>      | <span data-ttu-id="56a5a-215">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-215">False</span></span>                                 |
| <span data-ttu-id="56a5a-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56a5a-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="56a5a-217">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="56a5a-217">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="56a5a-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56a5a-218">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="56a5a-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56a5a-219">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="56a5a-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56a5a-220">Search-Flags</span></span>           | <span data-ttu-id="56a5a-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56a5a-221">0x00000000</span></span>                            |
| <span data-ttu-id="56a5a-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56a5a-222">System-Flags</span></span>           | <span data-ttu-id="56a5a-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56a5a-223">0x00000010</span></span>                            |
| <span data-ttu-id="56a5a-224">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="56a5a-224">Classes used in</span></span>        | [<span data-ttu-id="56a5a-225">**Servers**</span><span class="sxs-lookup"><span data-stu-id="56a5a-225">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="56a5a-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56a5a-226">Windows Server 2008</span></span>



| <span data-ttu-id="56a5a-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56a5a-227">Entry</span></span> | <span data-ttu-id="56a5a-228">Wert</span><span class="sxs-lookup"><span data-stu-id="56a5a-228">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="56a5a-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="56a5a-229">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="56a5a-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56a5a-230">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="56a5a-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="56a5a-231">System-Only</span></span>            | <span data-ttu-id="56a5a-232">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-232">False</span></span>                                 |
| <span data-ttu-id="56a5a-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="56a5a-233">Is-Single-Valued</span></span>       | <span data-ttu-id="56a5a-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="56a5a-234">True</span></span>                                  |
| <span data-ttu-id="56a5a-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="56a5a-235">Is Indexed</span></span>             | <span data-ttu-id="56a5a-236">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-236">False</span></span>                                 |
| <span data-ttu-id="56a5a-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="56a5a-237">In Global Catalog</span></span>      | <span data-ttu-id="56a5a-238">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-238">False</span></span>                                 |
| <span data-ttu-id="56a5a-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56a5a-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="56a5a-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="56a5a-240">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="56a5a-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56a5a-241">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="56a5a-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56a5a-242">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="56a5a-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56a5a-243">Search-Flags</span></span>           | <span data-ttu-id="56a5a-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56a5a-244">0x00000000</span></span>                            |
| <span data-ttu-id="56a5a-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56a5a-245">System-Flags</span></span>           | <span data-ttu-id="56a5a-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56a5a-246">0x00000010</span></span>                            |
| <span data-ttu-id="56a5a-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="56a5a-247">Classes used in</span></span>        | [<span data-ttu-id="56a5a-248">**Servers**</span><span class="sxs-lookup"><span data-stu-id="56a5a-248">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="56a5a-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="56a5a-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="56a5a-250">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56a5a-250">Entry</span></span> | <span data-ttu-id="56a5a-251">Wert</span><span class="sxs-lookup"><span data-stu-id="56a5a-251">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="56a5a-252">Link-ID</span><span class="sxs-lookup"><span data-stu-id="56a5a-252">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="56a5a-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56a5a-253">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="56a5a-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="56a5a-254">System-Only</span></span>            | <span data-ttu-id="56a5a-255">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-255">False</span></span>                                 |
| <span data-ttu-id="56a5a-256">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="56a5a-256">Is-Single-Valued</span></span>       | <span data-ttu-id="56a5a-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="56a5a-257">True</span></span>                                  |
| <span data-ttu-id="56a5a-258">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="56a5a-258">Is Indexed</span></span>             | <span data-ttu-id="56a5a-259">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-259">False</span></span>                                 |
| <span data-ttu-id="56a5a-260">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="56a5a-260">In Global Catalog</span></span>      | <span data-ttu-id="56a5a-261">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-261">False</span></span>                                 |
| <span data-ttu-id="56a5a-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56a5a-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="56a5a-263">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="56a5a-263">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="56a5a-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56a5a-264">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="56a5a-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56a5a-265">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="56a5a-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56a5a-266">Search-Flags</span></span>           | <span data-ttu-id="56a5a-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56a5a-267">0x00000000</span></span>                            |
| <span data-ttu-id="56a5a-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56a5a-268">System-Flags</span></span>           | <span data-ttu-id="56a5a-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56a5a-269">0x00000010</span></span>                            |
| <span data-ttu-id="56a5a-270">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="56a5a-270">Classes used in</span></span>        | [<span data-ttu-id="56a5a-271">**Servers**</span><span class="sxs-lookup"><span data-stu-id="56a5a-271">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="56a5a-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="56a5a-272">Windows Server 2012</span></span>



| <span data-ttu-id="56a5a-273">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56a5a-273">Entry</span></span> | <span data-ttu-id="56a5a-274">Wert</span><span class="sxs-lookup"><span data-stu-id="56a5a-274">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="56a5a-275">Link-ID</span><span class="sxs-lookup"><span data-stu-id="56a5a-275">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="56a5a-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="56a5a-276">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="56a5a-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="56a5a-277">System-Only</span></span>            | <span data-ttu-id="56a5a-278">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-278">False</span></span>                                 |
| <span data-ttu-id="56a5a-279">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="56a5a-279">Is-Single-Valued</span></span>       | <span data-ttu-id="56a5a-280">Richtig</span><span class="sxs-lookup"><span data-stu-id="56a5a-280">True</span></span>                                  |
| <span data-ttu-id="56a5a-281">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="56a5a-281">Is Indexed</span></span>             | <span data-ttu-id="56a5a-282">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-282">False</span></span>                                 |
| <span data-ttu-id="56a5a-283">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="56a5a-283">In Global Catalog</span></span>      | <span data-ttu-id="56a5a-284">False</span><span class="sxs-lookup"><span data-stu-id="56a5a-284">False</span></span>                                 |
| <span data-ttu-id="56a5a-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="56a5a-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="56a5a-286">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="56a5a-286">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="56a5a-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="56a5a-287">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="56a5a-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="56a5a-288">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="56a5a-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="56a5a-289">Search-Flags</span></span>           | <span data-ttu-id="56a5a-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="56a5a-290">0x00000000</span></span>                            |
| <span data-ttu-id="56a5a-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="56a5a-291">System-Flags</span></span>           | <span data-ttu-id="56a5a-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="56a5a-292">0x00000010</span></span>                            |
| <span data-ttu-id="56a5a-293">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="56a5a-293">Classes used in</span></span>        | [<span data-ttu-id="56a5a-294">**Servers**</span><span class="sxs-lookup"><span data-stu-id="56a5a-294">**Server**</span></span>](c-server.md)<br/> |



 

 





