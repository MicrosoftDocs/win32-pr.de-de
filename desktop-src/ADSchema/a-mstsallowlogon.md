---
title: MS-TS-Allow-Logon-Attribut
description: Gibt an, ob der Benutzer sich am Terminal Server anmelden darf. Der Wert ist 1, wenn die Anmeldung zulässig ist, und 0, wenn die Anmeldung nicht zulässig ist.
ms.assetid: 9cd6edbc-f8e7-4933-9f62-1e34e3d31fb7
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-TS-Allow-Logon-Attribut
- AD-Schema des mstsallowlogon-Attributs
topic_type:
- apiref
api_name:
- ms-TS-Allow-Logon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcd78662167e281ea720f2ad5d98f25c2f5c4ae
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859627"
---
# <a name="ms-ts-allow-logon-attribute"></a><span data-ttu-id="5ab21-106">MS-TS-Allow-Logon-Attribut</span><span class="sxs-lookup"><span data-stu-id="5ab21-106">ms-TS-Allow-Logon attribute</span></span>

<span data-ttu-id="5ab21-107">Gibt an, ob der Benutzer sich am Terminal Server anmelden darf.</span><span class="sxs-lookup"><span data-stu-id="5ab21-107">Specifies whether the user is allowed to log on to the Terminal Server.</span></span> <span data-ttu-id="5ab21-108">Der Wert ist 1, wenn die Anmeldung zulässig ist, und 0, wenn die Anmeldung nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="5ab21-108">The value is 1 if logon is allowed, and 0 if logon is not allowed.</span></span>



| <span data-ttu-id="5ab21-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ab21-109">Entry</span></span> | <span data-ttu-id="5ab21-110">Wert</span><span class="sxs-lookup"><span data-stu-id="5ab21-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5ab21-111">CN</span><span class="sxs-lookup"><span data-stu-id="5ab21-111">CN</span></span>                | <span data-ttu-id="5ab21-112">MS-TS-Allow-LOGON</span><span class="sxs-lookup"><span data-stu-id="5ab21-112">ms-TS-Allow-Logon</span></span>                    |
| <span data-ttu-id="5ab21-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5ab21-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5ab21-114">mstsallowlogon</span><span class="sxs-lookup"><span data-stu-id="5ab21-114">msTSAllowLogon</span></span>                       |
| <span data-ttu-id="5ab21-115">Size</span><span class="sxs-lookup"><span data-stu-id="5ab21-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="5ab21-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5ab21-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="5ab21-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="5ab21-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="5ab21-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5ab21-118">Attribute-Id</span></span>      | <span data-ttu-id="5ab21-119">1.2.840.113556.1.4.1979</span><span class="sxs-lookup"><span data-stu-id="5ab21-119">1.2.840.113556.1.4.1979</span></span>              |
| <span data-ttu-id="5ab21-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5ab21-120">System-Id-Guid</span></span>    | <span data-ttu-id="5ab21-121">3a0cd464-bc54-40e7-93ae-a646a6ecc4b4</span><span class="sxs-lookup"><span data-stu-id="5ab21-121">3a0cd464-bc54-40e7-93ae-a646a6ecc4b4</span></span> |
| <span data-ttu-id="5ab21-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ab21-122">Syntax</span></span>            | [<span data-ttu-id="5ab21-123">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="5ab21-123">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="5ab21-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="5ab21-124">Implementations</span></span>

-   [<span data-ttu-id="5ab21-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5ab21-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5ab21-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5ab21-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5ab21-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5ab21-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="5ab21-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ab21-128">Windows Server 2008</span></span>



| <span data-ttu-id="5ab21-129">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ab21-129">Entry</span></span> | <span data-ttu-id="5ab21-130">Wert</span><span class="sxs-lookup"><span data-stu-id="5ab21-130">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="5ab21-131">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5ab21-131">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="5ab21-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ab21-132">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="5ab21-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ab21-133">System-Only</span></span>            | <span data-ttu-id="5ab21-134">False</span><span class="sxs-lookup"><span data-stu-id="5ab21-134">False</span></span>                             |
| <span data-ttu-id="5ab21-135">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5ab21-135">Is-Single-Valued</span></span>       | <span data-ttu-id="5ab21-136">Richtig</span><span class="sxs-lookup"><span data-stu-id="5ab21-136">True</span></span>                              |
| <span data-ttu-id="5ab21-137">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5ab21-137">Is Indexed</span></span>             | <span data-ttu-id="5ab21-138">False</span><span class="sxs-lookup"><span data-stu-id="5ab21-138">False</span></span>                             |
| <span data-ttu-id="5ab21-139">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5ab21-139">In Global Catalog</span></span>      | <span data-ttu-id="5ab21-140">False</span><span class="sxs-lookup"><span data-stu-id="5ab21-140">False</span></span>                             |
| <span data-ttu-id="5ab21-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5ab21-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ab21-142">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5ab21-142">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="5ab21-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ab21-143">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="5ab21-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ab21-144">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="5ab21-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ab21-145">Search-Flags</span></span>           | <span data-ttu-id="5ab21-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ab21-146">0x00000000</span></span>                        |
| <span data-ttu-id="5ab21-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ab21-147">System-Flags</span></span>           | <span data-ttu-id="5ab21-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5ab21-148">0x00000010</span></span>                        |
| <span data-ttu-id="5ab21-149">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5ab21-149">Classes used in</span></span>        | [<span data-ttu-id="5ab21-150">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="5ab21-150">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5ab21-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5ab21-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5ab21-152">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ab21-152">Entry</span></span> | <span data-ttu-id="5ab21-153">Wert</span><span class="sxs-lookup"><span data-stu-id="5ab21-153">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="5ab21-154">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5ab21-154">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="5ab21-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ab21-155">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="5ab21-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ab21-156">System-Only</span></span>            | <span data-ttu-id="5ab21-157">False</span><span class="sxs-lookup"><span data-stu-id="5ab21-157">False</span></span>                             |
| <span data-ttu-id="5ab21-158">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5ab21-158">Is-Single-Valued</span></span>       | <span data-ttu-id="5ab21-159">Richtig</span><span class="sxs-lookup"><span data-stu-id="5ab21-159">True</span></span>                              |
| <span data-ttu-id="5ab21-160">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5ab21-160">Is Indexed</span></span>             | <span data-ttu-id="5ab21-161">False</span><span class="sxs-lookup"><span data-stu-id="5ab21-161">False</span></span>                             |
| <span data-ttu-id="5ab21-162">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5ab21-162">In Global Catalog</span></span>      | <span data-ttu-id="5ab21-163">False</span><span class="sxs-lookup"><span data-stu-id="5ab21-163">False</span></span>                             |
| <span data-ttu-id="5ab21-164">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5ab21-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ab21-165">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5ab21-165">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="5ab21-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ab21-166">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="5ab21-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ab21-167">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="5ab21-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ab21-168">Search-Flags</span></span>           | <span data-ttu-id="5ab21-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ab21-169">0x00000000</span></span>                        |
| <span data-ttu-id="5ab21-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ab21-170">System-Flags</span></span>           | <span data-ttu-id="5ab21-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5ab21-171">0x00000010</span></span>                        |
| <span data-ttu-id="5ab21-172">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5ab21-172">Classes used in</span></span>        | [<span data-ttu-id="5ab21-173">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="5ab21-173">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5ab21-174">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ab21-174">Windows Server 2012</span></span>



| <span data-ttu-id="5ab21-175">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ab21-175">Entry</span></span> | <span data-ttu-id="5ab21-176">Wert</span><span class="sxs-lookup"><span data-stu-id="5ab21-176">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="5ab21-177">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5ab21-177">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="5ab21-178">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ab21-178">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="5ab21-179">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ab21-179">System-Only</span></span>            | <span data-ttu-id="5ab21-180">False</span><span class="sxs-lookup"><span data-stu-id="5ab21-180">False</span></span>                             |
| <span data-ttu-id="5ab21-181">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5ab21-181">Is-Single-Valued</span></span>       | <span data-ttu-id="5ab21-182">Richtig</span><span class="sxs-lookup"><span data-stu-id="5ab21-182">True</span></span>                              |
| <span data-ttu-id="5ab21-183">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5ab21-183">Is Indexed</span></span>             | <span data-ttu-id="5ab21-184">False</span><span class="sxs-lookup"><span data-stu-id="5ab21-184">False</span></span>                             |
| <span data-ttu-id="5ab21-185">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5ab21-185">In Global Catalog</span></span>      | <span data-ttu-id="5ab21-186">False</span><span class="sxs-lookup"><span data-stu-id="5ab21-186">False</span></span>                             |
| <span data-ttu-id="5ab21-187">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5ab21-187">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ab21-188">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5ab21-188">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="5ab21-189">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ab21-189">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="5ab21-190">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ab21-190">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="5ab21-191">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ab21-191">Search-Flags</span></span>           | <span data-ttu-id="5ab21-192">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ab21-192">0x00000000</span></span>                        |
| <span data-ttu-id="5ab21-193">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ab21-193">System-Flags</span></span>           | <span data-ttu-id="5ab21-194">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5ab21-194">0x00000010</span></span>                        |
| <span data-ttu-id="5ab21-195">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5ab21-195">Classes used in</span></span>        | [<span data-ttu-id="5ab21-196">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="5ab21-196">**User**</span></span>](c-user.md)<br/> |



 

 





