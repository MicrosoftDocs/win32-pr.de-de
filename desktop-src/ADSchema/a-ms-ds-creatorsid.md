---
title: MS-DS-Creator-SID-Attribut
description: Die Sicherheits-ID des Erstellers des Objekts, das dieses Attribut enthält.
ms.assetid: 5e643c56-bfe9-4489-89a9-5ce56f90f288
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-Creator-SID-Attribut
- AD-Schema des ms-DS-kreatorsid-Attributs
topic_type:
- apiref
api_name:
- MS-DS-Creator-SID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b5b5635773271c4864ac2c8ec1898edcc9a9f9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957370"
---
# <a name="ms-ds-creator-sid-attribute"></a><span data-ttu-id="a9b7c-105">MS-DS-Creator-SID-Attribut</span><span class="sxs-lookup"><span data-stu-id="a9b7c-105">MS-DS-Creator-SID attribute</span></span>

<span data-ttu-id="a9b7c-106">Die Sicherheits-ID des Erstellers des Objekts, das dieses Attribut enthält.</span><span class="sxs-lookup"><span data-stu-id="a9b7c-106">The security ID of the creator of the object that contains this attribute.</span></span>



| <span data-ttu-id="a9b7c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a9b7c-107">Entry</span></span> | <span data-ttu-id="a9b7c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="a9b7c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a9b7c-109">CN</span><span class="sxs-lookup"><span data-stu-id="a9b7c-109">CN</span></span>                | <span data-ttu-id="a9b7c-110">MS-DS-Creator-sid</span><span class="sxs-lookup"><span data-stu-id="a9b7c-110">MS-DS-Creator-SID</span></span>                    |
| <span data-ttu-id="a9b7c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a9b7c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a9b7c-112">mS-DS-kreatorsid</span><span class="sxs-lookup"><span data-stu-id="a9b7c-112">mS-DS-CreatorSID</span></span>                     |
| <span data-ttu-id="a9b7c-113">Size</span><span class="sxs-lookup"><span data-stu-id="a9b7c-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="a9b7c-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a9b7c-114">Update Privilege</span></span>  | <span data-ttu-id="a9b7c-115">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a9b7c-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="a9b7c-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="a9b7c-116">Update Frequency</span></span>  | <span data-ttu-id="a9b7c-117">Jedes Mal, wenn ein neues-Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a9b7c-117">Whenever a new object is created.</span></span>    |
| <span data-ttu-id="a9b7c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a9b7c-118">Attribute-Id</span></span>      | <span data-ttu-id="a9b7c-119">1.2.840.113556.1.4.1410</span><span class="sxs-lookup"><span data-stu-id="a9b7c-119">1.2.840.113556.1.4.1410</span></span>              |
| <span data-ttu-id="a9b7c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a9b7c-120">System-Id-Guid</span></span>    | <span data-ttu-id="a9b7c-121">c5e60132-1480-11d3-91c1-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="a9b7c-121">c5e60132-1480-11d3-91c1-0000f87a57d4</span></span> |
| <span data-ttu-id="a9b7c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9b7c-122">Syntax</span></span>            | [<span data-ttu-id="a9b7c-123">**Zeichenfolge (SID)**</span><span class="sxs-lookup"><span data-stu-id="a9b7c-123">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="a9b7c-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="a9b7c-124">Implementations</span></span>

-   [<span data-ttu-id="a9b7c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a9b7c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a9b7c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a9b7c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a9b7c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a9b7c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a9b7c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a9b7c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a9b7c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a9b7c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a9b7c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a9b7c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a9b7c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a9b7c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a9b7c-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a9b7c-132">Entry</span></span> | <span data-ttu-id="a9b7c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="a9b7c-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a9b7c-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a9b7c-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a9b7c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9b7c-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a9b7c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9b7c-136">System-Only</span></span>            | <span data-ttu-id="a9b7c-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-137">True</span></span>                              |
| <span data-ttu-id="a9b7c-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a9b7c-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-139">True</span></span>                              |
| <span data-ttu-id="a9b7c-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a9b7c-140">Is Indexed</span></span>             | <span data-ttu-id="a9b7c-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-141">True</span></span>                              |
| <span data-ttu-id="a9b7c-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a9b7c-142">In Global Catalog</span></span>      | <span data-ttu-id="a9b7c-143">False</span><span class="sxs-lookup"><span data-stu-id="a9b7c-143">False</span></span>                             |
| <span data-ttu-id="a9b7c-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a9b7c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9b7c-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a9b7c-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a9b7c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9b7c-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a9b7c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9b7c-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a9b7c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9b7c-148">Search-Flags</span></span>           | <span data-ttu-id="a9b7c-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a9b7c-149">0x00000001</span></span>                        |
| <span data-ttu-id="a9b7c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9b7c-150">System-Flags</span></span>           | <span data-ttu-id="a9b7c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9b7c-151">0x00000010</span></span>                        |
| <span data-ttu-id="a9b7c-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a9b7c-152">Classes used in</span></span>        | [<span data-ttu-id="a9b7c-153">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="a9b7c-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a9b7c-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a9b7c-154">Windows Server 2003</span></span>



| <span data-ttu-id="a9b7c-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a9b7c-155">Entry</span></span> | <span data-ttu-id="a9b7c-156">Wert</span><span class="sxs-lookup"><span data-stu-id="a9b7c-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a9b7c-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a9b7c-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a9b7c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9b7c-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a9b7c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9b7c-159">System-Only</span></span>            | <span data-ttu-id="a9b7c-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-160">True</span></span>                              |
| <span data-ttu-id="a9b7c-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a9b7c-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-162">True</span></span>                              |
| <span data-ttu-id="a9b7c-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a9b7c-163">Is Indexed</span></span>             | <span data-ttu-id="a9b7c-164">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-164">True</span></span>                              |
| <span data-ttu-id="a9b7c-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a9b7c-165">In Global Catalog</span></span>      | <span data-ttu-id="a9b7c-166">False</span><span class="sxs-lookup"><span data-stu-id="a9b7c-166">False</span></span>                             |
| <span data-ttu-id="a9b7c-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a9b7c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9b7c-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a9b7c-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a9b7c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9b7c-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a9b7c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9b7c-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a9b7c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9b7c-171">Search-Flags</span></span>           | <span data-ttu-id="a9b7c-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a9b7c-172">0x00000001</span></span>                        |
| <span data-ttu-id="a9b7c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9b7c-173">System-Flags</span></span>           | <span data-ttu-id="a9b7c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9b7c-174">0x00000010</span></span>                        |
| <span data-ttu-id="a9b7c-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a9b7c-175">Classes used in</span></span>        | [<span data-ttu-id="a9b7c-176">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="a9b7c-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a9b7c-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a9b7c-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a9b7c-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a9b7c-178">Entry</span></span> | <span data-ttu-id="a9b7c-179">Wert</span><span class="sxs-lookup"><span data-stu-id="a9b7c-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a9b7c-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a9b7c-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a9b7c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9b7c-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a9b7c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9b7c-182">System-Only</span></span>            | <span data-ttu-id="a9b7c-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-183">True</span></span>                              |
| <span data-ttu-id="a9b7c-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a9b7c-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-185">True</span></span>                              |
| <span data-ttu-id="a9b7c-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a9b7c-186">Is Indexed</span></span>             | <span data-ttu-id="a9b7c-187">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-187">True</span></span>                              |
| <span data-ttu-id="a9b7c-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a9b7c-188">In Global Catalog</span></span>      | <span data-ttu-id="a9b7c-189">False</span><span class="sxs-lookup"><span data-stu-id="a9b7c-189">False</span></span>                             |
| <span data-ttu-id="a9b7c-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a9b7c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9b7c-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a9b7c-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a9b7c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9b7c-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a9b7c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9b7c-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a9b7c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9b7c-194">Search-Flags</span></span>           | <span data-ttu-id="a9b7c-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a9b7c-195">0x00000001</span></span>                        |
| <span data-ttu-id="a9b7c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9b7c-196">System-Flags</span></span>           | <span data-ttu-id="a9b7c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9b7c-197">0x00000010</span></span>                        |
| <span data-ttu-id="a9b7c-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a9b7c-198">Classes used in</span></span>        | [<span data-ttu-id="a9b7c-199">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="a9b7c-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a9b7c-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9b7c-200">Windows Server 2008</span></span>



| <span data-ttu-id="a9b7c-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a9b7c-201">Entry</span></span> | <span data-ttu-id="a9b7c-202">Wert</span><span class="sxs-lookup"><span data-stu-id="a9b7c-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a9b7c-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a9b7c-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a9b7c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9b7c-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a9b7c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9b7c-205">System-Only</span></span>            | <span data-ttu-id="a9b7c-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-206">True</span></span>                              |
| <span data-ttu-id="a9b7c-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a9b7c-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-208">True</span></span>                              |
| <span data-ttu-id="a9b7c-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a9b7c-209">Is Indexed</span></span>             | <span data-ttu-id="a9b7c-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-210">True</span></span>                              |
| <span data-ttu-id="a9b7c-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a9b7c-211">In Global Catalog</span></span>      | <span data-ttu-id="a9b7c-212">False</span><span class="sxs-lookup"><span data-stu-id="a9b7c-212">False</span></span>                             |
| <span data-ttu-id="a9b7c-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a9b7c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9b7c-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a9b7c-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a9b7c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9b7c-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a9b7c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9b7c-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a9b7c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9b7c-217">Search-Flags</span></span>           | <span data-ttu-id="a9b7c-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a9b7c-218">0x00000001</span></span>                        |
| <span data-ttu-id="a9b7c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9b7c-219">System-Flags</span></span>           | <span data-ttu-id="a9b7c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9b7c-220">0x00000010</span></span>                        |
| <span data-ttu-id="a9b7c-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a9b7c-221">Classes used in</span></span>        | [<span data-ttu-id="a9b7c-222">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="a9b7c-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a9b7c-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a9b7c-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a9b7c-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a9b7c-224">Entry</span></span> | <span data-ttu-id="a9b7c-225">Wert</span><span class="sxs-lookup"><span data-stu-id="a9b7c-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a9b7c-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a9b7c-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a9b7c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9b7c-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a9b7c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9b7c-228">System-Only</span></span>            | <span data-ttu-id="a9b7c-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-229">True</span></span>                              |
| <span data-ttu-id="a9b7c-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a9b7c-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-231">True</span></span>                              |
| <span data-ttu-id="a9b7c-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a9b7c-232">Is Indexed</span></span>             | <span data-ttu-id="a9b7c-233">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-233">True</span></span>                              |
| <span data-ttu-id="a9b7c-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a9b7c-234">In Global Catalog</span></span>      | <span data-ttu-id="a9b7c-235">False</span><span class="sxs-lookup"><span data-stu-id="a9b7c-235">False</span></span>                             |
| <span data-ttu-id="a9b7c-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a9b7c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9b7c-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a9b7c-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a9b7c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9b7c-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a9b7c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9b7c-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a9b7c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9b7c-240">Search-Flags</span></span>           | <span data-ttu-id="a9b7c-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a9b7c-241">0x00000001</span></span>                        |
| <span data-ttu-id="a9b7c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9b7c-242">System-Flags</span></span>           | <span data-ttu-id="a9b7c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9b7c-243">0x00000010</span></span>                        |
| <span data-ttu-id="a9b7c-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a9b7c-244">Classes used in</span></span>        | [<span data-ttu-id="a9b7c-245">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="a9b7c-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a9b7c-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9b7c-246">Windows Server 2012</span></span>



| <span data-ttu-id="a9b7c-247">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a9b7c-247">Entry</span></span> | <span data-ttu-id="a9b7c-248">Wert</span><span class="sxs-lookup"><span data-stu-id="a9b7c-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a9b7c-249">Link-ID</span><span class="sxs-lookup"><span data-stu-id="a9b7c-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a9b7c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9b7c-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a9b7c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9b7c-251">System-Only</span></span>            | <span data-ttu-id="a9b7c-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-252">True</span></span>                              |
| <span data-ttu-id="a9b7c-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a9b7c-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-254">True</span></span>                              |
| <span data-ttu-id="a9b7c-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="a9b7c-255">Is Indexed</span></span>             | <span data-ttu-id="a9b7c-256">Richtig</span><span class="sxs-lookup"><span data-stu-id="a9b7c-256">True</span></span>                              |
| <span data-ttu-id="a9b7c-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="a9b7c-257">In Global Catalog</span></span>      | <span data-ttu-id="a9b7c-258">False</span><span class="sxs-lookup"><span data-stu-id="a9b7c-258">False</span></span>                             |
| <span data-ttu-id="a9b7c-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a9b7c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9b7c-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="a9b7c-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a9b7c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9b7c-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a9b7c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9b7c-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a9b7c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9b7c-263">Search-Flags</span></span>           | <span data-ttu-id="a9b7c-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a9b7c-264">0x00000001</span></span>                        |
| <span data-ttu-id="a9b7c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9b7c-265">System-Flags</span></span>           | <span data-ttu-id="a9b7c-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9b7c-266">0x00000010</span></span>                        |
| <span data-ttu-id="a9b7c-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="a9b7c-267">Classes used in</span></span>        | [<span data-ttu-id="a9b7c-268">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="a9b7c-268">**User**</span></span>](c-user.md)<br/> |



 

 





