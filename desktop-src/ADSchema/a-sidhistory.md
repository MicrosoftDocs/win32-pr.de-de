---
title: SID-History-Attribut
description: Enthält vorherige SIDs, die für das-Objekt verwendet werden, wenn das Objekt aus einer anderen Domäne verschoben wurde.
ms.assetid: d738002b-fc05-4c60-aaf9-b83be61ed5a9
ms.tgt_platform: multiple
keywords:
- AD-Schema für SID-History-Attribut
- SIDHistory-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- SID-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16474a6463fc99e7ed2c1d2b1a2cdbf6ea9b6614
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479922"
---
# <a name="sid-history-attribute"></a><span data-ttu-id="743dd-105">SID-History-Attribut</span><span class="sxs-lookup"><span data-stu-id="743dd-105">SID-History attribute</span></span>

<span data-ttu-id="743dd-106">Enthält vorherige SIDs, die für das-Objekt verwendet werden, wenn das Objekt aus einer anderen Domäne verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="743dd-106">Contains previous SIDs used for the object if the object was moved from another domain.</span></span> <span data-ttu-id="743dd-107">Wenn ein Objekt von einer Domäne in eine andere verschoben wird, wird eine neue SID erstellt, und diese neue SID wird zur objectSID.</span><span class="sxs-lookup"><span data-stu-id="743dd-107">Whenever an object is moved from one domain to another, a new SID is created and that new SID becomes the objectSID.</span></span> <span data-ttu-id="743dd-108">Die vorherige sid wird der SIDHistory-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="743dd-108">The previous SID is added to the sIDHistory property.</span></span>



| <span data-ttu-id="743dd-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="743dd-109">Entry</span></span> | <span data-ttu-id="743dd-110">Wert</span><span class="sxs-lookup"><span data-stu-id="743dd-110">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="743dd-111">CN</span><span class="sxs-lookup"><span data-stu-id="743dd-111">CN</span></span>                | <span data-ttu-id="743dd-112">SID-History</span><span class="sxs-lookup"><span data-stu-id="743dd-112">SID-History</span></span>                                    |
| <span data-ttu-id="743dd-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="743dd-113">Ldap-Display-Name</span></span> | <span data-ttu-id="743dd-114">SIDHistory</span><span class="sxs-lookup"><span data-stu-id="743dd-114">sIDHistory</span></span>                                     |
| <span data-ttu-id="743dd-115">Size</span><span class="sxs-lookup"><span data-stu-id="743dd-115">Size</span></span>              | \-                                             |
| <span data-ttu-id="743dd-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="743dd-116">Update Privilege</span></span>  | <span data-ttu-id="743dd-117">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="743dd-117">This value is set by the system.</span></span>               |
| <span data-ttu-id="743dd-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="743dd-118">Update Frequency</span></span>  | <span data-ttu-id="743dd-119">Jedes Mal, wenn das Objekt in eine neue Domäne verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="743dd-119">Each time the object is moved to a new domain.</span></span> |
| <span data-ttu-id="743dd-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="743dd-120">Attribute-Id</span></span>      | <span data-ttu-id="743dd-121">1.2.840.113556.1.4.609</span><span class="sxs-lookup"><span data-stu-id="743dd-121">1.2.840.113556.1.4.609</span></span>                         |
| <span data-ttu-id="743dd-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="743dd-122">System-Id-Guid</span></span>    | <span data-ttu-id="743dd-123">17eb4278-D167-11D0-B002-0000,</span><span class="sxs-lookup"><span data-stu-id="743dd-123">17eb4278-d167-11d0-b002-0000f80367c1</span></span>           |
| <span data-ttu-id="743dd-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="743dd-124">Syntax</span></span>            | [<span data-ttu-id="743dd-125">**Zeichenfolge (SID)**</span><span class="sxs-lookup"><span data-stu-id="743dd-125">**String(Sid)**</span></span>](s-string-sid.md)            |



## <a name="implementations"></a><span data-ttu-id="743dd-126">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="743dd-126">Implementations</span></span>

-   [<span data-ttu-id="743dd-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="743dd-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="743dd-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="743dd-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="743dd-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="743dd-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="743dd-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="743dd-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="743dd-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="743dd-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="743dd-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="743dd-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="743dd-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="743dd-133">Windows 2000 Server</span></span>



| <span data-ttu-id="743dd-134">Eingabe</span><span class="sxs-lookup"><span data-stu-id="743dd-134">Entry</span></span> | <span data-ttu-id="743dd-135">Wert</span><span class="sxs-lookup"><span data-stu-id="743dd-135">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="743dd-136">Link-ID</span><span class="sxs-lookup"><span data-stu-id="743dd-136">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="743dd-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="743dd-137">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="743dd-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="743dd-138">System-Only</span></span>            | <span data-ttu-id="743dd-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="743dd-139">True</span></span>                                                         |
| <span data-ttu-id="743dd-140">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="743dd-140">Is-Single-Valued</span></span>       | <span data-ttu-id="743dd-141">False</span><span class="sxs-lookup"><span data-stu-id="743dd-141">False</span></span>                                                        |
| <span data-ttu-id="743dd-142">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="743dd-142">Is Indexed</span></span>             | <span data-ttu-id="743dd-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="743dd-143">True</span></span>                                                         |
| <span data-ttu-id="743dd-144">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="743dd-144">In Global Catalog</span></span>      | <span data-ttu-id="743dd-145">Richtig</span><span class="sxs-lookup"><span data-stu-id="743dd-145">True</span></span>                                                         |
| <span data-ttu-id="743dd-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="743dd-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="743dd-147">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="743dd-147">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="743dd-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="743dd-148">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="743dd-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="743dd-149">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="743dd-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="743dd-150">Search-Flags</span></span>           | <span data-ttu-id="743dd-151">0x00000001</span><span class="sxs-lookup"><span data-stu-id="743dd-151">0x00000001</span></span>                                                   |
| <span data-ttu-id="743dd-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="743dd-152">System-Flags</span></span>           | <span data-ttu-id="743dd-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="743dd-153">0x00000012</span></span>                                                   |
| <span data-ttu-id="743dd-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="743dd-154">Classes used in</span></span>        | [<span data-ttu-id="743dd-155">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="743dd-155">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="743dd-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="743dd-156">Windows Server 2003</span></span>



| <span data-ttu-id="743dd-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="743dd-157">Entry</span></span> | <span data-ttu-id="743dd-158">Wert</span><span class="sxs-lookup"><span data-stu-id="743dd-158">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="743dd-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="743dd-159">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="743dd-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="743dd-160">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="743dd-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="743dd-161">System-Only</span></span>            | <span data-ttu-id="743dd-162">False</span><span class="sxs-lookup"><span data-stu-id="743dd-162">False</span></span>                                                        |
| <span data-ttu-id="743dd-163">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="743dd-163">Is-Single-Valued</span></span>       | <span data-ttu-id="743dd-164">False</span><span class="sxs-lookup"><span data-stu-id="743dd-164">False</span></span>                                                        |
| <span data-ttu-id="743dd-165">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="743dd-165">Is Indexed</span></span>             | <span data-ttu-id="743dd-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="743dd-166">True</span></span>                                                         |
| <span data-ttu-id="743dd-167">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="743dd-167">In Global Catalog</span></span>      | <span data-ttu-id="743dd-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="743dd-168">True</span></span>                                                         |
| <span data-ttu-id="743dd-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="743dd-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="743dd-170">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="743dd-170">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="743dd-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="743dd-171">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="743dd-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="743dd-172">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="743dd-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="743dd-173">Search-Flags</span></span>           | <span data-ttu-id="743dd-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="743dd-174">0x00000001</span></span>                                                   |
| <span data-ttu-id="743dd-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="743dd-175">System-Flags</span></span>           | <span data-ttu-id="743dd-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="743dd-176">0x00000012</span></span>                                                   |
| <span data-ttu-id="743dd-177">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="743dd-177">Classes used in</span></span>        | [<span data-ttu-id="743dd-178">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="743dd-178">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="743dd-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="743dd-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="743dd-180">Eingabe</span><span class="sxs-lookup"><span data-stu-id="743dd-180">Entry</span></span> | <span data-ttu-id="743dd-181">Wert</span><span class="sxs-lookup"><span data-stu-id="743dd-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="743dd-182">Link-ID</span><span class="sxs-lookup"><span data-stu-id="743dd-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="743dd-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="743dd-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="743dd-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="743dd-184">System-Only</span></span>            | <span data-ttu-id="743dd-185">False</span><span class="sxs-lookup"><span data-stu-id="743dd-185">False</span></span>                                                        |
| <span data-ttu-id="743dd-186">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="743dd-186">Is-Single-Valued</span></span>       | <span data-ttu-id="743dd-187">False</span><span class="sxs-lookup"><span data-stu-id="743dd-187">False</span></span>                                                        |
| <span data-ttu-id="743dd-188">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="743dd-188">Is Indexed</span></span>             | <span data-ttu-id="743dd-189">Richtig</span><span class="sxs-lookup"><span data-stu-id="743dd-189">True</span></span>                                                         |
| <span data-ttu-id="743dd-190">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="743dd-190">In Global Catalog</span></span>      | <span data-ttu-id="743dd-191">Richtig</span><span class="sxs-lookup"><span data-stu-id="743dd-191">True</span></span>                                                         |
| <span data-ttu-id="743dd-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="743dd-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="743dd-193">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="743dd-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="743dd-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="743dd-194">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="743dd-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="743dd-195">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="743dd-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="743dd-196">Search-Flags</span></span>           | <span data-ttu-id="743dd-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="743dd-197">0x00000001</span></span>                                                   |
| <span data-ttu-id="743dd-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="743dd-198">System-Flags</span></span>           | <span data-ttu-id="743dd-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="743dd-199">0x00000012</span></span>                                                   |
| <span data-ttu-id="743dd-200">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="743dd-200">Classes used in</span></span>        | [<span data-ttu-id="743dd-201">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="743dd-201">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="743dd-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="743dd-202">Windows Server 2008</span></span>



| <span data-ttu-id="743dd-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="743dd-203">Entry</span></span> | <span data-ttu-id="743dd-204">Wert</span><span class="sxs-lookup"><span data-stu-id="743dd-204">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="743dd-205">Link-ID</span><span class="sxs-lookup"><span data-stu-id="743dd-205">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="743dd-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="743dd-206">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="743dd-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="743dd-207">System-Only</span></span>            | <span data-ttu-id="743dd-208">False</span><span class="sxs-lookup"><span data-stu-id="743dd-208">False</span></span>                                                        |
| <span data-ttu-id="743dd-209">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="743dd-209">Is-Single-Valued</span></span>       | <span data-ttu-id="743dd-210">False</span><span class="sxs-lookup"><span data-stu-id="743dd-210">False</span></span>                                                        |
| <span data-ttu-id="743dd-211">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="743dd-211">Is Indexed</span></span>             | <span data-ttu-id="743dd-212">Richtig</span><span class="sxs-lookup"><span data-stu-id="743dd-212">True</span></span>                                                         |
| <span data-ttu-id="743dd-213">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="743dd-213">In Global Catalog</span></span>      | <span data-ttu-id="743dd-214">Richtig</span><span class="sxs-lookup"><span data-stu-id="743dd-214">True</span></span>                                                         |
| <span data-ttu-id="743dd-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="743dd-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="743dd-216">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="743dd-216">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="743dd-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="743dd-217">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="743dd-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="743dd-218">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="743dd-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="743dd-219">Search-Flags</span></span>           | <span data-ttu-id="743dd-220">0x00000001</span><span class="sxs-lookup"><span data-stu-id="743dd-220">0x00000001</span></span>                                                   |
| <span data-ttu-id="743dd-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="743dd-221">System-Flags</span></span>           | <span data-ttu-id="743dd-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="743dd-222">0x00000012</span></span>                                                   |
| <span data-ttu-id="743dd-223">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="743dd-223">Classes used in</span></span>        | [<span data-ttu-id="743dd-224">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="743dd-224">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="743dd-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="743dd-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="743dd-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="743dd-226">Entry</span></span> | <span data-ttu-id="743dd-227">Wert</span><span class="sxs-lookup"><span data-stu-id="743dd-227">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="743dd-228">Link-ID</span><span class="sxs-lookup"><span data-stu-id="743dd-228">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="743dd-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="743dd-229">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="743dd-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="743dd-230">System-Only</span></span>            | <span data-ttu-id="743dd-231">False</span><span class="sxs-lookup"><span data-stu-id="743dd-231">False</span></span>                                                        |
| <span data-ttu-id="743dd-232">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="743dd-232">Is-Single-Valued</span></span>       | <span data-ttu-id="743dd-233">False</span><span class="sxs-lookup"><span data-stu-id="743dd-233">False</span></span>                                                        |
| <span data-ttu-id="743dd-234">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="743dd-234">Is Indexed</span></span>             | <span data-ttu-id="743dd-235">Richtig</span><span class="sxs-lookup"><span data-stu-id="743dd-235">True</span></span>                                                         |
| <span data-ttu-id="743dd-236">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="743dd-236">In Global Catalog</span></span>      | <span data-ttu-id="743dd-237">Richtig</span><span class="sxs-lookup"><span data-stu-id="743dd-237">True</span></span>                                                         |
| <span data-ttu-id="743dd-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="743dd-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="743dd-239">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="743dd-239">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="743dd-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="743dd-240">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="743dd-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="743dd-241">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="743dd-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="743dd-242">Search-Flags</span></span>           | <span data-ttu-id="743dd-243">0x00000001</span><span class="sxs-lookup"><span data-stu-id="743dd-243">0x00000001</span></span>                                                   |
| <span data-ttu-id="743dd-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="743dd-244">System-Flags</span></span>           | <span data-ttu-id="743dd-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="743dd-245">0x00000012</span></span>                                                   |
| <span data-ttu-id="743dd-246">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="743dd-246">Classes used in</span></span>        | [<span data-ttu-id="743dd-247">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="743dd-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="743dd-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="743dd-248">Windows Server 2012</span></span>



| <span data-ttu-id="743dd-249">Eingabe</span><span class="sxs-lookup"><span data-stu-id="743dd-249">Entry</span></span> | <span data-ttu-id="743dd-250">Wert</span><span class="sxs-lookup"><span data-stu-id="743dd-250">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="743dd-251">Link-ID</span><span class="sxs-lookup"><span data-stu-id="743dd-251">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="743dd-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="743dd-252">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="743dd-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="743dd-253">System-Only</span></span>            | <span data-ttu-id="743dd-254">False</span><span class="sxs-lookup"><span data-stu-id="743dd-254">False</span></span>                                                        |
| <span data-ttu-id="743dd-255">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="743dd-255">Is-Single-Valued</span></span>       | <span data-ttu-id="743dd-256">False</span><span class="sxs-lookup"><span data-stu-id="743dd-256">False</span></span>                                                        |
| <span data-ttu-id="743dd-257">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="743dd-257">Is Indexed</span></span>             | <span data-ttu-id="743dd-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="743dd-258">True</span></span>                                                         |
| <span data-ttu-id="743dd-259">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="743dd-259">In Global Catalog</span></span>      | <span data-ttu-id="743dd-260">Richtig</span><span class="sxs-lookup"><span data-stu-id="743dd-260">True</span></span>                                                         |
| <span data-ttu-id="743dd-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="743dd-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="743dd-262">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="743dd-262">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="743dd-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="743dd-263">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="743dd-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="743dd-264">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="743dd-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="743dd-265">Search-Flags</span></span>           | <span data-ttu-id="743dd-266">0x00000001</span><span class="sxs-lookup"><span data-stu-id="743dd-266">0x00000001</span></span>                                                   |
| <span data-ttu-id="743dd-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="743dd-267">System-Flags</span></span>           | <span data-ttu-id="743dd-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="743dd-268">0x00000012</span></span>                                                   |
| <span data-ttu-id="743dd-269">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="743dd-269">Classes used in</span></span>        | [<span data-ttu-id="743dd-270">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="743dd-270">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





