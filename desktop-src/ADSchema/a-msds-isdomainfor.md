---
title: ms-DS-is-Domain-for-Attribut
description: Rückwärts Verknüpfung für ms-DS-has-Domain-NCS. Gibt an, welche DCS diese Partition als primäre Domäne enthalten. | ms-DS-is-Domain-for-Attribut
ms.assetid: ec63ddb4-c220-492b-92ce-e3da2069bcb8
ms.tgt_platform: multiple
keywords:
- ms-DS-is-Domain-für Attribut-AD-Schema
- MSDS-isdomainfor-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-DS-Is-Domain-For
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56529497eb8081f53310e26b834194cdcdc11bf5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365034"
---
# <a name="ms-ds-is-domain-for-attribute"></a><span data-ttu-id="3aa17-107">ms-DS-is-Domain-for-Attribut</span><span class="sxs-lookup"><span data-stu-id="3aa17-107">ms-DS-Is-Domain-For attribute</span></span>

<span data-ttu-id="3aa17-108">Rückwärts Verknüpfung für [**ms-DS-has-Domain-NCS**](a-msds-hasdomainncs.md).</span><span class="sxs-lookup"><span data-stu-id="3aa17-108">Backward link for [**ms-DS-Has-Domain-NCs**](a-msds-hasdomainncs.md).</span></span> <span data-ttu-id="3aa17-109">Gibt an, welche DCS diese Partition als primäre Domäne enthalten.</span><span class="sxs-lookup"><span data-stu-id="3aa17-109">Identifies which DCs hold that partition as their primary domain.</span></span>



| <span data-ttu-id="3aa17-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3aa17-110">Entry</span></span> | <span data-ttu-id="3aa17-111">Wert</span><span class="sxs-lookup"><span data-stu-id="3aa17-111">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="3aa17-112">CN</span><span class="sxs-lookup"><span data-stu-id="3aa17-112">CN</span></span>                | <span data-ttu-id="3aa17-113">ms-DS-is-Domain-for</span><span class="sxs-lookup"><span data-stu-id="3aa17-113">ms-DS-Is-Domain-For</span></span>                     |
| <span data-ttu-id="3aa17-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3aa17-114">Ldap-Display-Name</span></span> | <span data-ttu-id="3aa17-115">MSDS-isdomainfor</span><span class="sxs-lookup"><span data-stu-id="3aa17-115">msDS-IsDomainFor</span></span>                        |
| <span data-ttu-id="3aa17-116">Size</span><span class="sxs-lookup"><span data-stu-id="3aa17-116">Size</span></span>              | \-                                      |
| <span data-ttu-id="3aa17-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="3aa17-117">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="3aa17-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="3aa17-118">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="3aa17-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3aa17-119">Attribute-Id</span></span>      | <span data-ttu-id="3aa17-120">1.2.840.113556.1.4.1933</span><span class="sxs-lookup"><span data-stu-id="3aa17-120">1.2.840.113556.1.4.1933</span></span>                 |
| <span data-ttu-id="3aa17-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3aa17-121">System-Id-Guid</span></span>    | <span data-ttu-id="3aa17-122">ff155a2a-44e5-4de0-8318-13a58988de4f</span><span class="sxs-lookup"><span data-stu-id="3aa17-122">ff155a2a-44e5-4de0-8318-13a58988de4f</span></span>    |
| <span data-ttu-id="3aa17-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="3aa17-123">Syntax</span></span>            | [<span data-ttu-id="3aa17-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="3aa17-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="3aa17-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="3aa17-125">Implementations</span></span>

-   [<span data-ttu-id="3aa17-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3aa17-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3aa17-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3aa17-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3aa17-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3aa17-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="3aa17-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3aa17-129">Windows Server 2008</span></span>



| <span data-ttu-id="3aa17-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3aa17-130">Entry</span></span> | <span data-ttu-id="3aa17-131">Wert</span><span class="sxs-lookup"><span data-stu-id="3aa17-131">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3aa17-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3aa17-132">Link-Id</span></span>                | <span data-ttu-id="3aa17-133">2027</span><span class="sxs-lookup"><span data-stu-id="3aa17-133">2027</span></span>                            |
| <span data-ttu-id="3aa17-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3aa17-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3aa17-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="3aa17-135">System-Only</span></span>            | <span data-ttu-id="3aa17-136">Richtig</span><span class="sxs-lookup"><span data-stu-id="3aa17-136">True</span></span>                            |
| <span data-ttu-id="3aa17-137">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3aa17-137">Is-Single-Valued</span></span>       | <span data-ttu-id="3aa17-138">False</span><span class="sxs-lookup"><span data-stu-id="3aa17-138">False</span></span>                           |
| <span data-ttu-id="3aa17-139">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3aa17-139">Is Indexed</span></span>             | <span data-ttu-id="3aa17-140">False</span><span class="sxs-lookup"><span data-stu-id="3aa17-140">False</span></span>                           |
| <span data-ttu-id="3aa17-141">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3aa17-141">In Global Catalog</span></span>      | <span data-ttu-id="3aa17-142">False</span><span class="sxs-lookup"><span data-stu-id="3aa17-142">False</span></span>                           |
| <span data-ttu-id="3aa17-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3aa17-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="3aa17-144">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3aa17-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3aa17-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3aa17-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3aa17-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3aa17-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3aa17-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa17-147">Search-Flags</span></span>           | <span data-ttu-id="3aa17-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aa17-148">0x00000000</span></span>                      |
| <span data-ttu-id="3aa17-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa17-149">System-Flags</span></span>           | <span data-ttu-id="3aa17-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="3aa17-150">0x00000011</span></span>                      |
| <span data-ttu-id="3aa17-151">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3aa17-151">Classes used in</span></span>        | [<span data-ttu-id="3aa17-152">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="3aa17-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3aa17-153">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3aa17-153">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3aa17-154">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3aa17-154">Entry</span></span> | <span data-ttu-id="3aa17-155">Wert</span><span class="sxs-lookup"><span data-stu-id="3aa17-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3aa17-156">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3aa17-156">Link-Id</span></span>                | <span data-ttu-id="3aa17-157">2027</span><span class="sxs-lookup"><span data-stu-id="3aa17-157">2027</span></span>                            |
| <span data-ttu-id="3aa17-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3aa17-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3aa17-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="3aa17-159">System-Only</span></span>            | <span data-ttu-id="3aa17-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="3aa17-160">True</span></span>                            |
| <span data-ttu-id="3aa17-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3aa17-161">Is-Single-Valued</span></span>       | <span data-ttu-id="3aa17-162">False</span><span class="sxs-lookup"><span data-stu-id="3aa17-162">False</span></span>                           |
| <span data-ttu-id="3aa17-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3aa17-163">Is Indexed</span></span>             | <span data-ttu-id="3aa17-164">False</span><span class="sxs-lookup"><span data-stu-id="3aa17-164">False</span></span>                           |
| <span data-ttu-id="3aa17-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3aa17-165">In Global Catalog</span></span>      | <span data-ttu-id="3aa17-166">False</span><span class="sxs-lookup"><span data-stu-id="3aa17-166">False</span></span>                           |
| <span data-ttu-id="3aa17-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3aa17-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="3aa17-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3aa17-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3aa17-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3aa17-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3aa17-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3aa17-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3aa17-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa17-171">Search-Flags</span></span>           | <span data-ttu-id="3aa17-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aa17-172">0x00000000</span></span>                      |
| <span data-ttu-id="3aa17-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa17-173">System-Flags</span></span>           | <span data-ttu-id="3aa17-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="3aa17-174">0x00000011</span></span>                      |
| <span data-ttu-id="3aa17-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3aa17-175">Classes used in</span></span>        | [<span data-ttu-id="3aa17-176">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="3aa17-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3aa17-177">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3aa17-177">Windows Server 2012</span></span>



| <span data-ttu-id="3aa17-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3aa17-178">Entry</span></span> | <span data-ttu-id="3aa17-179">Wert</span><span class="sxs-lookup"><span data-stu-id="3aa17-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3aa17-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="3aa17-180">Link-Id</span></span>                | <span data-ttu-id="3aa17-181">2027</span><span class="sxs-lookup"><span data-stu-id="3aa17-181">2027</span></span>                            |
| <span data-ttu-id="3aa17-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3aa17-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="3aa17-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="3aa17-183">System-Only</span></span>            | <span data-ttu-id="3aa17-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="3aa17-184">True</span></span>                            |
| <span data-ttu-id="3aa17-185">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="3aa17-185">Is-Single-Valued</span></span>       | <span data-ttu-id="3aa17-186">False</span><span class="sxs-lookup"><span data-stu-id="3aa17-186">False</span></span>                           |
| <span data-ttu-id="3aa17-187">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="3aa17-187">Is Indexed</span></span>             | <span data-ttu-id="3aa17-188">False</span><span class="sxs-lookup"><span data-stu-id="3aa17-188">False</span></span>                           |
| <span data-ttu-id="3aa17-189">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="3aa17-189">In Global Catalog</span></span>      | <span data-ttu-id="3aa17-190">False</span><span class="sxs-lookup"><span data-stu-id="3aa17-190">False</span></span>                           |
| <span data-ttu-id="3aa17-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3aa17-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="3aa17-192">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="3aa17-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3aa17-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3aa17-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3aa17-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3aa17-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3aa17-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa17-195">Search-Flags</span></span>           | <span data-ttu-id="3aa17-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3aa17-196">0x00000000</span></span>                      |
| <span data-ttu-id="3aa17-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3aa17-197">System-Flags</span></span>           | <span data-ttu-id="3aa17-198">0x00000011</span><span class="sxs-lookup"><span data-stu-id="3aa17-198">0x00000011</span></span>                      |
| <span data-ttu-id="3aa17-199">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="3aa17-199">Classes used in</span></span>        | [<span data-ttu-id="3aa17-200">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="3aa17-200">**Top**</span></span>](c-top.md)<br/> |



 

 





