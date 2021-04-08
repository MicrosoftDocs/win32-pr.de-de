---
title: Nachname-Attribut
description: Dieses Attribut enthält die Familie oder den Nachnamen eines Benutzers.
ms.assetid: d9d53c9f-4efa-47c4-aec4-518fb8a868b3
ms.tgt_platform: multiple
keywords:
- Namens Schema des Nachnamen-Attributs
- Schema des SN-Attributs AD
topic_type:
- apiref
api_name:
- Surname
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453352574a7aec10c56492060ac2de6ceeca030f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957440"
---
# <a name="surname-attribute"></a><span data-ttu-id="7a3d5-105">Nachname-Attribut</span><span class="sxs-lookup"><span data-stu-id="7a3d5-105">Surname attribute</span></span>

<span data-ttu-id="7a3d5-106">Dieses Attribut enthält die Familie oder den Nachnamen eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="7a3d5-106">This attribute contains the family or last name for a user.</span></span>



| <span data-ttu-id="7a3d5-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a3d5-107">Entry</span></span> | <span data-ttu-id="7a3d5-108">Wert</span><span class="sxs-lookup"><span data-stu-id="7a3d5-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7a3d5-109">CN</span><span class="sxs-lookup"><span data-stu-id="7a3d5-109">CN</span></span>                | <span data-ttu-id="7a3d5-110">Surname</span><span class="sxs-lookup"><span data-stu-id="7a3d5-110">Surname</span></span>                                                                          |
| <span data-ttu-id="7a3d5-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7a3d5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7a3d5-112">sn</span><span class="sxs-lookup"><span data-stu-id="7a3d5-112">sn</span></span>                                                                               |
| <span data-ttu-id="7a3d5-113">Size</span><span class="sxs-lookup"><span data-stu-id="7a3d5-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="7a3d5-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="7a3d5-114">Update Privilege</span></span>  | <span data-ttu-id="7a3d5-115">Jeder kann dieses Objekt basierend auf der Sicherheit des Objekts, das erstellt wird, aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7a3d5-115">Anyone may update this object based on the security of the object being created.</span></span> |
| <span data-ttu-id="7a3d5-116">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="7a3d5-116">Update Frequency</span></span>  | \-                                                                               |
| <span data-ttu-id="7a3d5-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7a3d5-117">Attribute-Id</span></span>      | <span data-ttu-id="7a3d5-118">2.5.4.4</span><span class="sxs-lookup"><span data-stu-id="7a3d5-118">2.5.4.4</span></span>                                                                          |
| <span data-ttu-id="7a3d5-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7a3d5-119">System-Id-Guid</span></span>    | <span data-ttu-id="7a3d5-120">bf967a41-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7a3d5-120">bf967a41-0de6-11d0-a285-00aa003049e2</span></span>                                             |
| <span data-ttu-id="7a3d5-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a3d5-121">Syntax</span></span>            | [<span data-ttu-id="7a3d5-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-122">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="7a3d5-123">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="7a3d5-123">Implementations</span></span>

-   [<span data-ttu-id="7a3d5-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7a3d5-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7a3d5-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7a3d5-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7a3d5-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7a3d5-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7a3d5-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7a3d5-130">Windows 2000 Server</span></span>



| <span data-ttu-id="7a3d5-131">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a3d5-131">Entry</span></span> | <span data-ttu-id="7a3d5-132">Wert</span><span class="sxs-lookup"><span data-stu-id="7a3d5-132">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="7a3d5-133">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7a3d5-133">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="7a3d5-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a3d5-134">MAPI-Id</span></span>                | <span data-ttu-id="7a3d5-135">0x3a11</span><span class="sxs-lookup"><span data-stu-id="7a3d5-135">0x3A11</span></span>                                |
| <span data-ttu-id="7a3d5-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a3d5-136">System-Only</span></span>            | <span data-ttu-id="7a3d5-137">False</span><span class="sxs-lookup"><span data-stu-id="7a3d5-137">False</span></span>                                 |
| <span data-ttu-id="7a3d5-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7a3d5-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-139">True</span></span>                                  |
| <span data-ttu-id="7a3d5-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7a3d5-140">Is Indexed</span></span>             | <span data-ttu-id="7a3d5-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-141">True</span></span>                                  |
| <span data-ttu-id="7a3d5-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7a3d5-142">In Global Catalog</span></span>      | <span data-ttu-id="7a3d5-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-143">True</span></span>                                  |
| <span data-ttu-id="7a3d5-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a3d5-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a3d5-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7a3d5-145">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="7a3d5-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a3d5-146">Range-Lower</span></span>            | <span data-ttu-id="7a3d5-147">1</span><span class="sxs-lookup"><span data-stu-id="7a3d5-147">1</span></span>                                     |
| <span data-ttu-id="7a3d5-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a3d5-148">Range-Upper</span></span>            | <span data-ttu-id="7a3d5-149">64</span><span class="sxs-lookup"><span data-stu-id="7a3d5-149">64</span></span>                                    |
| <span data-ttu-id="7a3d5-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a3d5-150">Search-Flags</span></span>           | <span data-ttu-id="7a3d5-151">0x00000005</span><span class="sxs-lookup"><span data-stu-id="7a3d5-151">0x00000005</span></span>                            |
| <span data-ttu-id="7a3d5-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a3d5-152">System-Flags</span></span>           | <span data-ttu-id="7a3d5-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a3d5-153">0x00000010</span></span>                            |
| <span data-ttu-id="7a3d5-154">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7a3d5-154">Classes used in</span></span>        | [<span data-ttu-id="7a3d5-155">**Person**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-155">**Person**</span></span>](c-person.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7a3d5-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7a3d5-156">Windows Server 2003</span></span>



| <span data-ttu-id="7a3d5-157">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a3d5-157">Entry</span></span> | <span data-ttu-id="7a3d5-158">Wert</span><span class="sxs-lookup"><span data-stu-id="7a3d5-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a3d5-159">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7a3d5-159">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="7a3d5-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a3d5-160">MAPI-Id</span></span>                | <span data-ttu-id="7a3d5-161">0x3a11</span><span class="sxs-lookup"><span data-stu-id="7a3d5-161">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="7a3d5-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a3d5-162">System-Only</span></span>            | <span data-ttu-id="7a3d5-163">False</span><span class="sxs-lookup"><span data-stu-id="7a3d5-163">False</span></span>                                                                                         |
| <span data-ttu-id="7a3d5-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-164">Is-Single-Valued</span></span>       | <span data-ttu-id="7a3d5-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-165">True</span></span>                                                                                          |
| <span data-ttu-id="7a3d5-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7a3d5-166">Is Indexed</span></span>             | <span data-ttu-id="7a3d5-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-167">True</span></span>                                                                                          |
| <span data-ttu-id="7a3d5-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7a3d5-168">In Global Catalog</span></span>      | <span data-ttu-id="7a3d5-169">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-169">True</span></span>                                                                                          |
| <span data-ttu-id="7a3d5-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a3d5-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a3d5-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7a3d5-171">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="7a3d5-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a3d5-172">Range-Lower</span></span>            | <span data-ttu-id="7a3d5-173">1</span><span class="sxs-lookup"><span data-stu-id="7a3d5-173">1</span></span>                                                                                             |
| <span data-ttu-id="7a3d5-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a3d5-174">Range-Upper</span></span>            | <span data-ttu-id="7a3d5-175">64</span><span class="sxs-lookup"><span data-stu-id="7a3d5-175">64</span></span>                                                                                            |
| <span data-ttu-id="7a3d5-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a3d5-176">Search-Flags</span></span>           | <span data-ttu-id="7a3d5-177">0x00000005</span><span class="sxs-lookup"><span data-stu-id="7a3d5-177">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="7a3d5-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a3d5-178">System-Flags</span></span>           | <span data-ttu-id="7a3d5-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a3d5-179">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="7a3d5-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7a3d5-180">Classes used in</span></span>        | [<span data-ttu-id="7a3d5-181">**Person**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-181">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="7a3d5-182">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-182">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7a3d5-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7a3d5-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7a3d5-184">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a3d5-184">Entry</span></span> | <span data-ttu-id="7a3d5-185">Wert</span><span class="sxs-lookup"><span data-stu-id="7a3d5-185">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a3d5-186">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7a3d5-186">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="7a3d5-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a3d5-187">MAPI-Id</span></span>                | <span data-ttu-id="7a3d5-188">0x3a11</span><span class="sxs-lookup"><span data-stu-id="7a3d5-188">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="7a3d5-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a3d5-189">System-Only</span></span>            | <span data-ttu-id="7a3d5-190">False</span><span class="sxs-lookup"><span data-stu-id="7a3d5-190">False</span></span>                                                                                         |
| <span data-ttu-id="7a3d5-191">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-191">Is-Single-Valued</span></span>       | <span data-ttu-id="7a3d5-192">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-192">True</span></span>                                                                                          |
| <span data-ttu-id="7a3d5-193">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7a3d5-193">Is Indexed</span></span>             | <span data-ttu-id="7a3d5-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-194">True</span></span>                                                                                          |
| <span data-ttu-id="7a3d5-195">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7a3d5-195">In Global Catalog</span></span>      | <span data-ttu-id="7a3d5-196">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-196">True</span></span>                                                                                          |
| <span data-ttu-id="7a3d5-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a3d5-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a3d5-198">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7a3d5-198">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="7a3d5-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a3d5-199">Range-Lower</span></span>            | <span data-ttu-id="7a3d5-200">1</span><span class="sxs-lookup"><span data-stu-id="7a3d5-200">1</span></span>                                                                                             |
| <span data-ttu-id="7a3d5-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a3d5-201">Range-Upper</span></span>            | <span data-ttu-id="7a3d5-202">64</span><span class="sxs-lookup"><span data-stu-id="7a3d5-202">64</span></span>                                                                                            |
| <span data-ttu-id="7a3d5-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a3d5-203">Search-Flags</span></span>           | <span data-ttu-id="7a3d5-204">0x00000005</span><span class="sxs-lookup"><span data-stu-id="7a3d5-204">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="7a3d5-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a3d5-205">System-Flags</span></span>           | <span data-ttu-id="7a3d5-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a3d5-206">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="7a3d5-207">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7a3d5-207">Classes used in</span></span>        | [<span data-ttu-id="7a3d5-208">**Person**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-208">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="7a3d5-209">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-209">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7a3d5-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a3d5-210">Windows Server 2008</span></span>



| <span data-ttu-id="7a3d5-211">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a3d5-211">Entry</span></span> | <span data-ttu-id="7a3d5-212">Wert</span><span class="sxs-lookup"><span data-stu-id="7a3d5-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a3d5-213">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7a3d5-213">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="7a3d5-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a3d5-214">MAPI-Id</span></span>                | <span data-ttu-id="7a3d5-215">0x3a11</span><span class="sxs-lookup"><span data-stu-id="7a3d5-215">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="7a3d5-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a3d5-216">System-Only</span></span>            | <span data-ttu-id="7a3d5-217">False</span><span class="sxs-lookup"><span data-stu-id="7a3d5-217">False</span></span>                                                                                         |
| <span data-ttu-id="7a3d5-218">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-218">Is-Single-Valued</span></span>       | <span data-ttu-id="7a3d5-219">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-219">True</span></span>                                                                                          |
| <span data-ttu-id="7a3d5-220">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7a3d5-220">Is Indexed</span></span>             | <span data-ttu-id="7a3d5-221">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-221">True</span></span>                                                                                          |
| <span data-ttu-id="7a3d5-222">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7a3d5-222">In Global Catalog</span></span>      | <span data-ttu-id="7a3d5-223">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-223">True</span></span>                                                                                          |
| <span data-ttu-id="7a3d5-224">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a3d5-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a3d5-225">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7a3d5-225">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="7a3d5-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a3d5-226">Range-Lower</span></span>            | <span data-ttu-id="7a3d5-227">1</span><span class="sxs-lookup"><span data-stu-id="7a3d5-227">1</span></span>                                                                                             |
| <span data-ttu-id="7a3d5-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a3d5-228">Range-Upper</span></span>            | <span data-ttu-id="7a3d5-229">64</span><span class="sxs-lookup"><span data-stu-id="7a3d5-229">64</span></span>                                                                                            |
| <span data-ttu-id="7a3d5-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a3d5-230">Search-Flags</span></span>           | <span data-ttu-id="7a3d5-231">0x00000005</span><span class="sxs-lookup"><span data-stu-id="7a3d5-231">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="7a3d5-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a3d5-232">System-Flags</span></span>           | <span data-ttu-id="7a3d5-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a3d5-233">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="7a3d5-234">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7a3d5-234">Classes used in</span></span>        | [<span data-ttu-id="7a3d5-235">**Person**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-235">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="7a3d5-236">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-236">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7a3d5-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7a3d5-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7a3d5-238">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a3d5-238">Entry</span></span> | <span data-ttu-id="7a3d5-239">Wert</span><span class="sxs-lookup"><span data-stu-id="7a3d5-239">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a3d5-240">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7a3d5-240">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="7a3d5-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a3d5-241">MAPI-Id</span></span>                | <span data-ttu-id="7a3d5-242">0x3a11</span><span class="sxs-lookup"><span data-stu-id="7a3d5-242">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="7a3d5-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a3d5-243">System-Only</span></span>            | <span data-ttu-id="7a3d5-244">False</span><span class="sxs-lookup"><span data-stu-id="7a3d5-244">False</span></span>                                                                                         |
| <span data-ttu-id="7a3d5-245">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-245">Is-Single-Valued</span></span>       | <span data-ttu-id="7a3d5-246">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-246">True</span></span>                                                                                          |
| <span data-ttu-id="7a3d5-247">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7a3d5-247">Is Indexed</span></span>             | <span data-ttu-id="7a3d5-248">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-248">True</span></span>                                                                                          |
| <span data-ttu-id="7a3d5-249">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7a3d5-249">In Global Catalog</span></span>      | <span data-ttu-id="7a3d5-250">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-250">True</span></span>                                                                                          |
| <span data-ttu-id="7a3d5-251">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a3d5-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a3d5-252">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7a3d5-252">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="7a3d5-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a3d5-253">Range-Lower</span></span>            | <span data-ttu-id="7a3d5-254">1</span><span class="sxs-lookup"><span data-stu-id="7a3d5-254">1</span></span>                                                                                             |
| <span data-ttu-id="7a3d5-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a3d5-255">Range-Upper</span></span>            | <span data-ttu-id="7a3d5-256">64</span><span class="sxs-lookup"><span data-stu-id="7a3d5-256">64</span></span>                                                                                            |
| <span data-ttu-id="7a3d5-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a3d5-257">Search-Flags</span></span>           | <span data-ttu-id="7a3d5-258">0x00000005</span><span class="sxs-lookup"><span data-stu-id="7a3d5-258">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="7a3d5-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a3d5-259">System-Flags</span></span>           | <span data-ttu-id="7a3d5-260">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a3d5-260">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="7a3d5-261">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7a3d5-261">Classes used in</span></span>        | [<span data-ttu-id="7a3d5-262">**Person**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-262">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="7a3d5-263">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-263">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7a3d5-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7a3d5-264">Windows Server 2012</span></span>



| <span data-ttu-id="7a3d5-265">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a3d5-265">Entry</span></span> | <span data-ttu-id="7a3d5-266">Wert</span><span class="sxs-lookup"><span data-stu-id="7a3d5-266">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a3d5-267">Link-ID</span><span class="sxs-lookup"><span data-stu-id="7a3d5-267">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="7a3d5-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a3d5-268">MAPI-Id</span></span>                | <span data-ttu-id="7a3d5-269">0x3a11</span><span class="sxs-lookup"><span data-stu-id="7a3d5-269">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="7a3d5-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a3d5-270">System-Only</span></span>            | <span data-ttu-id="7a3d5-271">False</span><span class="sxs-lookup"><span data-stu-id="7a3d5-271">False</span></span>                                                                                         |
| <span data-ttu-id="7a3d5-272">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-272">Is-Single-Valued</span></span>       | <span data-ttu-id="7a3d5-273">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-273">True</span></span>                                                                                          |
| <span data-ttu-id="7a3d5-274">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="7a3d5-274">Is Indexed</span></span>             | <span data-ttu-id="7a3d5-275">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-275">True</span></span>                                                                                          |
| <span data-ttu-id="7a3d5-276">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="7a3d5-276">In Global Catalog</span></span>      | <span data-ttu-id="7a3d5-277">Richtig</span><span class="sxs-lookup"><span data-stu-id="7a3d5-277">True</span></span>                                                                                          |
| <span data-ttu-id="7a3d5-278">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a3d5-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a3d5-279">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="7a3d5-279">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="7a3d5-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a3d5-280">Range-Lower</span></span>            | <span data-ttu-id="7a3d5-281">1</span><span class="sxs-lookup"><span data-stu-id="7a3d5-281">1</span></span>                                                                                             |
| <span data-ttu-id="7a3d5-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a3d5-282">Range-Upper</span></span>            | <span data-ttu-id="7a3d5-283">64</span><span class="sxs-lookup"><span data-stu-id="7a3d5-283">64</span></span>                                                                                            |
| <span data-ttu-id="7a3d5-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a3d5-284">Search-Flags</span></span>           | <span data-ttu-id="7a3d5-285">0x00000005</span><span class="sxs-lookup"><span data-stu-id="7a3d5-285">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="7a3d5-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a3d5-286">System-Flags</span></span>           | <span data-ttu-id="7a3d5-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a3d5-287">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="7a3d5-288">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="7a3d5-288">Classes used in</span></span>        | [<span data-ttu-id="7a3d5-289">**Person**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-289">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="7a3d5-290">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="7a3d5-290">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



 

 





