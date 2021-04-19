---
title: Dienst Prinzipal Name-Attribut
description: Liste der Prinzipal Namen, die für die gegenseitige Authentifizierung bei einer Instanz eines Dienstanbieter auf diesem Computer verwendet werden.
ms.assetid: 0ad1694f-0d6f-4350-a088-fdf3ef798c46
ms.tgt_platform: multiple
keywords:
- AD-Schema für Dienst Prinzipal Name-Attribut
- servicePrincipalName-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Service-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 861f160d2c9b71d2c9914c7ff9c2ea0ee43c8528
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344883"
---
# <a name="service-principal-name-attribute"></a><span data-ttu-id="d168f-105">Dienst Prinzipal Name-Attribut</span><span class="sxs-lookup"><span data-stu-id="d168f-105">Service-Principal-Name attribute</span></span>

<span data-ttu-id="d168f-106">Liste der Prinzipal Namen, die für die gegenseitige Authentifizierung bei einer Instanz eines Dienstanbieter auf diesem Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d168f-106">List of principal names used for mutual authentication with an instance of a service on this computer.</span></span>



| <span data-ttu-id="d168f-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d168f-107">Entry</span></span> | <span data-ttu-id="d168f-108">Wert</span><span class="sxs-lookup"><span data-stu-id="d168f-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d168f-109">CN</span><span class="sxs-lookup"><span data-stu-id="d168f-109">CN</span></span>                | <span data-ttu-id="d168f-110">Dienst Prinzipal Name</span><span class="sxs-lookup"><span data-stu-id="d168f-110">Service-Principal-Name</span></span>                      |
| <span data-ttu-id="d168f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d168f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d168f-112">servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d168f-112">servicePrincipalName</span></span>                        |
| <span data-ttu-id="d168f-113">Size</span><span class="sxs-lookup"><span data-stu-id="d168f-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="d168f-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d168f-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="d168f-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="d168f-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="d168f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d168f-116">Attribute-Id</span></span>      | <span data-ttu-id="d168f-117">1.2.840.113556.1.4.771</span><span class="sxs-lookup"><span data-stu-id="d168f-117">1.2.840.113556.1.4.771</span></span>                      |
| <span data-ttu-id="d168f-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d168f-118">System-Id-Guid</span></span>    | <span data-ttu-id="d168f-119">f3a64788-5306-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d168f-119">f3a64788-5306-11d1-a9c5-0000f80367c1</span></span>        |
| <span data-ttu-id="d168f-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="d168f-120">Syntax</span></span>            | [<span data-ttu-id="d168f-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d168f-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d168f-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="d168f-122">Implementations</span></span>

-   [<span data-ttu-id="d168f-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d168f-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d168f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d168f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d168f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d168f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d168f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d168f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d168f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d168f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d168f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d168f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d168f-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d168f-129">Windows 2000 Server</span></span>



| <span data-ttu-id="d168f-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d168f-130">Entry</span></span> | <span data-ttu-id="d168f-131">Wert</span><span class="sxs-lookup"><span data-stu-id="d168f-131">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d168f-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d168f-132">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d168f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d168f-133">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d168f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="d168f-134">System-Only</span></span>            | <span data-ttu-id="d168f-135">False</span><span class="sxs-lookup"><span data-stu-id="d168f-135">False</span></span>                             |
| <span data-ttu-id="d168f-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d168f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="d168f-137">False</span><span class="sxs-lookup"><span data-stu-id="d168f-137">False</span></span>                             |
| <span data-ttu-id="d168f-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d168f-138">Is Indexed</span></span>             | <span data-ttu-id="d168f-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="d168f-139">True</span></span>                              |
| <span data-ttu-id="d168f-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d168f-140">In Global Catalog</span></span>      | <span data-ttu-id="d168f-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="d168f-141">True</span></span>                              |
| <span data-ttu-id="d168f-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d168f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="d168f-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d168f-143">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d168f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d168f-144">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d168f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d168f-145">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d168f-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d168f-146">Search-Flags</span></span>           | <span data-ttu-id="d168f-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d168f-147">0x00000001</span></span>                        |
| <span data-ttu-id="d168f-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d168f-148">System-Flags</span></span>           | <span data-ttu-id="d168f-149">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d168f-149">0x00000012</span></span>                        |
| <span data-ttu-id="d168f-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d168f-150">Classes used in</span></span>        | [<span data-ttu-id="d168f-151">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="d168f-151">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d168f-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d168f-152">Windows Server 2003</span></span>



| <span data-ttu-id="d168f-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d168f-153">Entry</span></span> | <span data-ttu-id="d168f-154">Wert</span><span class="sxs-lookup"><span data-stu-id="d168f-154">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d168f-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d168f-155">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d168f-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d168f-156">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d168f-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="d168f-157">System-Only</span></span>            | <span data-ttu-id="d168f-158">False</span><span class="sxs-lookup"><span data-stu-id="d168f-158">False</span></span>                             |
| <span data-ttu-id="d168f-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d168f-159">Is-Single-Valued</span></span>       | <span data-ttu-id="d168f-160">False</span><span class="sxs-lookup"><span data-stu-id="d168f-160">False</span></span>                             |
| <span data-ttu-id="d168f-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d168f-161">Is Indexed</span></span>             | <span data-ttu-id="d168f-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="d168f-162">True</span></span>                              |
| <span data-ttu-id="d168f-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d168f-163">In Global Catalog</span></span>      | <span data-ttu-id="d168f-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="d168f-164">True</span></span>                              |
| <span data-ttu-id="d168f-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d168f-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="d168f-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d168f-166">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d168f-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d168f-167">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d168f-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d168f-168">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d168f-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d168f-169">Search-Flags</span></span>           | <span data-ttu-id="d168f-170">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d168f-170">0x00000001</span></span>                        |
| <span data-ttu-id="d168f-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d168f-171">System-Flags</span></span>           | <span data-ttu-id="d168f-172">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d168f-172">0x00000012</span></span>                        |
| <span data-ttu-id="d168f-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d168f-173">Classes used in</span></span>        | [<span data-ttu-id="d168f-174">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="d168f-174">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d168f-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d168f-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d168f-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d168f-176">Entry</span></span> | <span data-ttu-id="d168f-177">Wert</span><span class="sxs-lookup"><span data-stu-id="d168f-177">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d168f-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d168f-178">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d168f-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d168f-179">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d168f-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="d168f-180">System-Only</span></span>            | <span data-ttu-id="d168f-181">False</span><span class="sxs-lookup"><span data-stu-id="d168f-181">False</span></span>                             |
| <span data-ttu-id="d168f-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d168f-182">Is-Single-Valued</span></span>       | <span data-ttu-id="d168f-183">False</span><span class="sxs-lookup"><span data-stu-id="d168f-183">False</span></span>                             |
| <span data-ttu-id="d168f-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d168f-184">Is Indexed</span></span>             | <span data-ttu-id="d168f-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="d168f-185">True</span></span>                              |
| <span data-ttu-id="d168f-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d168f-186">In Global Catalog</span></span>      | <span data-ttu-id="d168f-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="d168f-187">True</span></span>                              |
| <span data-ttu-id="d168f-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d168f-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="d168f-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d168f-189">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d168f-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d168f-190">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d168f-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d168f-191">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d168f-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d168f-192">Search-Flags</span></span>           | <span data-ttu-id="d168f-193">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d168f-193">0x00000001</span></span>                        |
| <span data-ttu-id="d168f-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d168f-194">System-Flags</span></span>           | <span data-ttu-id="d168f-195">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d168f-195">0x00000012</span></span>                        |
| <span data-ttu-id="d168f-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d168f-196">Classes used in</span></span>        | [<span data-ttu-id="d168f-197">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="d168f-197">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d168f-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d168f-198">Windows Server 2008</span></span>



| <span data-ttu-id="d168f-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d168f-199">Entry</span></span> | <span data-ttu-id="d168f-200">Wert</span><span class="sxs-lookup"><span data-stu-id="d168f-200">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d168f-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d168f-201">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d168f-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d168f-202">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d168f-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="d168f-203">System-Only</span></span>            | <span data-ttu-id="d168f-204">False</span><span class="sxs-lookup"><span data-stu-id="d168f-204">False</span></span>                             |
| <span data-ttu-id="d168f-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d168f-205">Is-Single-Valued</span></span>       | <span data-ttu-id="d168f-206">False</span><span class="sxs-lookup"><span data-stu-id="d168f-206">False</span></span>                             |
| <span data-ttu-id="d168f-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d168f-207">Is Indexed</span></span>             | <span data-ttu-id="d168f-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="d168f-208">True</span></span>                              |
| <span data-ttu-id="d168f-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d168f-209">In Global Catalog</span></span>      | <span data-ttu-id="d168f-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="d168f-210">True</span></span>                              |
| <span data-ttu-id="d168f-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d168f-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="d168f-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d168f-212">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d168f-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d168f-213">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d168f-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d168f-214">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d168f-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d168f-215">Search-Flags</span></span>           | <span data-ttu-id="d168f-216">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d168f-216">0x00000001</span></span>                        |
| <span data-ttu-id="d168f-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d168f-217">System-Flags</span></span>           | <span data-ttu-id="d168f-218">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d168f-218">0x00000012</span></span>                        |
| <span data-ttu-id="d168f-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d168f-219">Classes used in</span></span>        | [<span data-ttu-id="d168f-220">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="d168f-220">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d168f-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d168f-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d168f-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d168f-222">Entry</span></span> | <span data-ttu-id="d168f-223">Wert</span><span class="sxs-lookup"><span data-stu-id="d168f-223">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d168f-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d168f-224">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d168f-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d168f-225">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d168f-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="d168f-226">System-Only</span></span>            | <span data-ttu-id="d168f-227">False</span><span class="sxs-lookup"><span data-stu-id="d168f-227">False</span></span>                             |
| <span data-ttu-id="d168f-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d168f-228">Is-Single-Valued</span></span>       | <span data-ttu-id="d168f-229">False</span><span class="sxs-lookup"><span data-stu-id="d168f-229">False</span></span>                             |
| <span data-ttu-id="d168f-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d168f-230">Is Indexed</span></span>             | <span data-ttu-id="d168f-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="d168f-231">True</span></span>                              |
| <span data-ttu-id="d168f-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d168f-232">In Global Catalog</span></span>      | <span data-ttu-id="d168f-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="d168f-233">True</span></span>                              |
| <span data-ttu-id="d168f-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d168f-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="d168f-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d168f-235">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d168f-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d168f-236">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d168f-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d168f-237">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d168f-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d168f-238">Search-Flags</span></span>           | <span data-ttu-id="d168f-239">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d168f-239">0x00000001</span></span>                        |
| <span data-ttu-id="d168f-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d168f-240">System-Flags</span></span>           | <span data-ttu-id="d168f-241">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d168f-241">0x00000012</span></span>                        |
| <span data-ttu-id="d168f-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d168f-242">Classes used in</span></span>        | [<span data-ttu-id="d168f-243">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="d168f-243">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d168f-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d168f-244">Windows Server 2012</span></span>



| <span data-ttu-id="d168f-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d168f-245">Entry</span></span> | <span data-ttu-id="d168f-246">Wert</span><span class="sxs-lookup"><span data-stu-id="d168f-246">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d168f-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d168f-247">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d168f-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d168f-248">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d168f-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="d168f-249">System-Only</span></span>            | <span data-ttu-id="d168f-250">False</span><span class="sxs-lookup"><span data-stu-id="d168f-250">False</span></span>                             |
| <span data-ttu-id="d168f-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d168f-251">Is-Single-Valued</span></span>       | <span data-ttu-id="d168f-252">False</span><span class="sxs-lookup"><span data-stu-id="d168f-252">False</span></span>                             |
| <span data-ttu-id="d168f-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d168f-253">Is Indexed</span></span>             | <span data-ttu-id="d168f-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="d168f-254">True</span></span>                              |
| <span data-ttu-id="d168f-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d168f-255">In Global Catalog</span></span>      | <span data-ttu-id="d168f-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="d168f-256">True</span></span>                              |
| <span data-ttu-id="d168f-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d168f-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="d168f-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d168f-258">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d168f-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d168f-259">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d168f-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d168f-260">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d168f-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d168f-261">Search-Flags</span></span>           | <span data-ttu-id="d168f-262">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d168f-262">0x00000001</span></span>                        |
| <span data-ttu-id="d168f-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d168f-263">System-Flags</span></span>           | <span data-ttu-id="d168f-264">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d168f-264">0x00000012</span></span>                        |
| <span data-ttu-id="d168f-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d168f-265">Classes used in</span></span>        | [<span data-ttu-id="d168f-266">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="d168f-266">**User**</span></span>](c-user.md)<br/> |



 

 





