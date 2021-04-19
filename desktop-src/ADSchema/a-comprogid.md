---
title: COM-ProgID-Attribut
description: Dieses Attribut speichert die Liste der COM-Objekt Programm-IDs, die in diesem Anwendungspaket implementiert werden.
ms.assetid: 9d2945e4-f236-48f6-bed3-145d445ff653
ms.tgt_platform: multiple
keywords:
- AD-Schema für COM-ProgID-Attribut
- comprogid-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- COM-ProgID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 686976732bedf2c4ba486186634720568d3b6c3c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106343533"
---
# <a name="com-progid-attribute"></a><span data-ttu-id="cf7ee-105">COM-ProgID-Attribut</span><span class="sxs-lookup"><span data-stu-id="cf7ee-105">COM-ProgID attribute</span></span>

<span data-ttu-id="cf7ee-106">Dieses Attribut speichert die Liste der COM-Objekt Programm-IDs, die in diesem Anwendungspaket implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="cf7ee-106">This attribute stores the list of COM object program IDs that are implemented in this application package.</span></span>



| <span data-ttu-id="cf7ee-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cf7ee-107">Entry</span></span> | <span data-ttu-id="cf7ee-108">Wert</span><span class="sxs-lookup"><span data-stu-id="cf7ee-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cf7ee-109">CN</span><span class="sxs-lookup"><span data-stu-id="cf7ee-109">CN</span></span>                | <span data-ttu-id="cf7ee-110">COM-ProgID</span><span class="sxs-lookup"><span data-stu-id="cf7ee-110">COM-ProgID</span></span>                                                                       |
| <span data-ttu-id="cf7ee-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cf7ee-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cf7ee-112">comprogid</span><span class="sxs-lookup"><span data-stu-id="cf7ee-112">cOMProgID</span></span>                                                                        |
| <span data-ttu-id="cf7ee-113">Size</span><span class="sxs-lookup"><span data-stu-id="cf7ee-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="cf7ee-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="cf7ee-114">Update Privilege</span></span>  | <span data-ttu-id="cf7ee-115">Jeder kann dieses Objekt basierend auf der Sicherheit des Objekts, das erstellt wird, aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="cf7ee-115">Anyone may update this object based on the security of the object being created.</span></span> |
| <span data-ttu-id="cf7ee-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="cf7ee-116">Update Frequency</span></span>  | \-                                                                               |
| <span data-ttu-id="cf7ee-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cf7ee-117">Attribute-Id</span></span>      | <span data-ttu-id="cf7ee-118">1.2.840.113556.1.4.21</span><span class="sxs-lookup"><span data-stu-id="cf7ee-118">1.2.840.113556.1.4.21</span></span>                                                            |
| <span data-ttu-id="cf7ee-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cf7ee-119">System-Id-Guid</span></span>    | <span data-ttu-id="cf7ee-120">bf96793d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="cf7ee-120">bf96793d-0de6-11d0-a285-00aa003049e2</span></span>                                             |
| <span data-ttu-id="cf7ee-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf7ee-121">Syntax</span></span>            | [<span data-ttu-id="cf7ee-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-122">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="cf7ee-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="cf7ee-123">Implementations</span></span>

-   [<span data-ttu-id="cf7ee-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cf7ee-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cf7ee-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cf7ee-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cf7ee-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cf7ee-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cf7ee-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cf7ee-130">Windows 2000 Server</span></span>



| <span data-ttu-id="cf7ee-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cf7ee-131">Entry</span></span> | <span data-ttu-id="cf7ee-132">Wert</span><span class="sxs-lookup"><span data-stu-id="cf7ee-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf7ee-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cf7ee-133">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf7ee-134">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf7ee-135">System-Only</span></span>            | <span data-ttu-id="cf7ee-136">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-136">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cf7ee-137">Is-Single-Valued</span></span>       | <span data-ttu-id="cf7ee-138">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-138">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cf7ee-139">Is Indexed</span></span>             | <span data-ttu-id="cf7ee-140">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-140">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cf7ee-141">In Global Catalog</span></span>      | <span data-ttu-id="cf7ee-142">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-142">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cf7ee-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf7ee-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cf7ee-144">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="cf7ee-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf7ee-145">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf7ee-146">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf7ee-147">Search-Flags</span></span>           | <span data-ttu-id="cf7ee-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf7ee-148">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="cf7ee-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf7ee-149">System-Flags</span></span>           | <span data-ttu-id="cf7ee-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf7ee-150">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="cf7ee-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cf7ee-151">Classes used in</span></span>        | [<span data-ttu-id="cf7ee-152">**Klassen Registrierung**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-152">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="cf7ee-153">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-153">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cf7ee-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cf7ee-154">Windows Server 2003</span></span>



| <span data-ttu-id="cf7ee-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cf7ee-155">Entry</span></span> | <span data-ttu-id="cf7ee-156">Wert</span><span class="sxs-lookup"><span data-stu-id="cf7ee-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf7ee-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cf7ee-157">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf7ee-158">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf7ee-159">System-Only</span></span>            | <span data-ttu-id="cf7ee-160">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-160">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cf7ee-161">Is-Single-Valued</span></span>       | <span data-ttu-id="cf7ee-162">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-162">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cf7ee-163">Is Indexed</span></span>             | <span data-ttu-id="cf7ee-164">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-164">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cf7ee-165">In Global Catalog</span></span>      | <span data-ttu-id="cf7ee-166">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-166">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cf7ee-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf7ee-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cf7ee-168">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="cf7ee-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf7ee-169">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf7ee-170">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf7ee-171">Search-Flags</span></span>           | <span data-ttu-id="cf7ee-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf7ee-172">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="cf7ee-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf7ee-173">System-Flags</span></span>           | <span data-ttu-id="cf7ee-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf7ee-174">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="cf7ee-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cf7ee-175">Classes used in</span></span>        | [<span data-ttu-id="cf7ee-176">**Klassen Registrierung**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-176">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="cf7ee-177">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-177">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cf7ee-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cf7ee-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cf7ee-179">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cf7ee-179">Entry</span></span> | <span data-ttu-id="cf7ee-180">Wert</span><span class="sxs-lookup"><span data-stu-id="cf7ee-180">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf7ee-181">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cf7ee-181">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf7ee-182">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf7ee-183">System-Only</span></span>            | <span data-ttu-id="cf7ee-184">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-184">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cf7ee-185">Is-Single-Valued</span></span>       | <span data-ttu-id="cf7ee-186">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-186">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cf7ee-187">Is Indexed</span></span>             | <span data-ttu-id="cf7ee-188">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-188">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cf7ee-189">In Global Catalog</span></span>      | <span data-ttu-id="cf7ee-190">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-190">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cf7ee-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf7ee-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cf7ee-192">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="cf7ee-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf7ee-193">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf7ee-194">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf7ee-195">Search-Flags</span></span>           | <span data-ttu-id="cf7ee-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf7ee-196">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="cf7ee-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf7ee-197">System-Flags</span></span>           | <span data-ttu-id="cf7ee-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf7ee-198">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="cf7ee-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cf7ee-199">Classes used in</span></span>        | [<span data-ttu-id="cf7ee-200">**Klassen Registrierung**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-200">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="cf7ee-201">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-201">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cf7ee-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf7ee-202">Windows Server 2008</span></span>



| <span data-ttu-id="cf7ee-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cf7ee-203">Entry</span></span> | <span data-ttu-id="cf7ee-204">Wert</span><span class="sxs-lookup"><span data-stu-id="cf7ee-204">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf7ee-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cf7ee-205">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf7ee-206">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf7ee-207">System-Only</span></span>            | <span data-ttu-id="cf7ee-208">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-208">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cf7ee-209">Is-Single-Valued</span></span>       | <span data-ttu-id="cf7ee-210">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-210">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cf7ee-211">Is Indexed</span></span>             | <span data-ttu-id="cf7ee-212">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-212">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cf7ee-213">In Global Catalog</span></span>      | <span data-ttu-id="cf7ee-214">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-214">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cf7ee-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf7ee-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cf7ee-216">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="cf7ee-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf7ee-217">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf7ee-218">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf7ee-219">Search-Flags</span></span>           | <span data-ttu-id="cf7ee-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf7ee-220">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="cf7ee-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf7ee-221">System-Flags</span></span>           | <span data-ttu-id="cf7ee-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf7ee-222">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="cf7ee-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cf7ee-223">Classes used in</span></span>        | [<span data-ttu-id="cf7ee-224">**Klassen Registrierung**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-224">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="cf7ee-225">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-225">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cf7ee-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cf7ee-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cf7ee-227">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cf7ee-227">Entry</span></span> | <span data-ttu-id="cf7ee-228">Wert</span><span class="sxs-lookup"><span data-stu-id="cf7ee-228">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf7ee-229">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cf7ee-229">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf7ee-230">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf7ee-231">System-Only</span></span>            | <span data-ttu-id="cf7ee-232">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-232">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-233">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cf7ee-233">Is-Single-Valued</span></span>       | <span data-ttu-id="cf7ee-234">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-234">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-235">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cf7ee-235">Is Indexed</span></span>             | <span data-ttu-id="cf7ee-236">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-236">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-237">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cf7ee-237">In Global Catalog</span></span>      | <span data-ttu-id="cf7ee-238">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-238">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cf7ee-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf7ee-240">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cf7ee-240">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="cf7ee-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf7ee-241">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf7ee-242">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf7ee-243">Search-Flags</span></span>           | <span data-ttu-id="cf7ee-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf7ee-244">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="cf7ee-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf7ee-245">System-Flags</span></span>           | <span data-ttu-id="cf7ee-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf7ee-246">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="cf7ee-247">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cf7ee-247">Classes used in</span></span>        | [<span data-ttu-id="cf7ee-248">**Klassen Registrierung**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-248">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="cf7ee-249">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-249">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cf7ee-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cf7ee-250">Windows Server 2012</span></span>



| <span data-ttu-id="cf7ee-251">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cf7ee-251">Entry</span></span> | <span data-ttu-id="cf7ee-252">Wert</span><span class="sxs-lookup"><span data-stu-id="cf7ee-252">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf7ee-253">Link-ID</span><span class="sxs-lookup"><span data-stu-id="cf7ee-253">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf7ee-254">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf7ee-255">System-Only</span></span>            | <span data-ttu-id="cf7ee-256">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-256">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-257">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="cf7ee-257">Is-Single-Valued</span></span>       | <span data-ttu-id="cf7ee-258">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-258">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-259">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="cf7ee-259">Is Indexed</span></span>             | <span data-ttu-id="cf7ee-260">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-260">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-261">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="cf7ee-261">In Global Catalog</span></span>      | <span data-ttu-id="cf7ee-262">False</span><span class="sxs-lookup"><span data-stu-id="cf7ee-262">False</span></span>                                                                                                                         |
| <span data-ttu-id="cf7ee-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cf7ee-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf7ee-264">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="cf7ee-264">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="cf7ee-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf7ee-265">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf7ee-266">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="cf7ee-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf7ee-267">Search-Flags</span></span>           | <span data-ttu-id="cf7ee-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf7ee-268">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="cf7ee-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf7ee-269">System-Flags</span></span>           | <span data-ttu-id="cf7ee-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf7ee-270">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="cf7ee-271">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="cf7ee-271">Classes used in</span></span>        | [<span data-ttu-id="cf7ee-272">**Klassen Registrierung**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-272">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="cf7ee-273">**Paket Registrierung**</span><span class="sxs-lookup"><span data-stu-id="cf7ee-273">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





