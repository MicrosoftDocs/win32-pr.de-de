---
title: ms-DS-default-Quota-Attribut
description: Das Standard Kontingent, das auf einen Sicherheits Prinzipal angewendet wird, der ein Objekt im NC erstellt, wenn keine Kontingent Spezifikation vorhanden ist, die den Sicherheits Prinzipal abdeckt.
ms.assetid: 48074aaa-3997-40ac-92fe-b3112408ab45
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-DS-default-Quota-Attributs
- AD-Schema des msDS-defaultquota-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Default-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d96f1429be72c623843608856da88729b1240c38
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957640"
---
# <a name="ms-ds-default-quota-attribute"></a><span data-ttu-id="8ae1e-105">ms-DS-default-Quota-Attribut</span><span class="sxs-lookup"><span data-stu-id="8ae1e-105">ms-DS-Default-Quota attribute</span></span>

<span data-ttu-id="8ae1e-106">Das Standard Kontingent, das auf einen Sicherheits Prinzipal angewendet wird, der ein Objekt im NC erstellt, wenn keine Kontingent Spezifikation vorhanden ist, die den Sicherheits Prinzipal abdeckt.</span><span class="sxs-lookup"><span data-stu-id="8ae1e-106">The default quota that will apply to a security principal that creates an object in the NC if no quota specification exists that covers the security principal.</span></span>



| <span data-ttu-id="8ae1e-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8ae1e-107">Entry</span></span> | <span data-ttu-id="8ae1e-108">Wert</span><span class="sxs-lookup"><span data-stu-id="8ae1e-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8ae1e-109">CN</span><span class="sxs-lookup"><span data-stu-id="8ae1e-109">CN</span></span>                | <span data-ttu-id="8ae1e-110">ms-DS-default-Quota</span><span class="sxs-lookup"><span data-stu-id="8ae1e-110">ms-DS-Default-Quota</span></span>                  |
| <span data-ttu-id="8ae1e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8ae1e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8ae1e-112">MSDS-defaultquota</span><span class="sxs-lookup"><span data-stu-id="8ae1e-112">msDS-DefaultQuota</span></span>                    |
| <span data-ttu-id="8ae1e-113">Size</span><span class="sxs-lookup"><span data-stu-id="8ae1e-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="8ae1e-114">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="8ae1e-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="8ae1e-115">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="8ae1e-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8ae1e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8ae1e-116">Attribute-Id</span></span>      | <span data-ttu-id="8ae1e-117">1.2.840.113556.1.4.1846</span><span class="sxs-lookup"><span data-stu-id="8ae1e-117">1.2.840.113556.1.4.1846</span></span>              |
| <span data-ttu-id="8ae1e-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8ae1e-118">System-Id-Guid</span></span>    | <span data-ttu-id="8ae1e-119">6818f 726-674b-441b-8a3a-f 40596374cea</span><span class="sxs-lookup"><span data-stu-id="8ae1e-119">6818f726-674b-441b-8a3a-f40596374cea</span></span> |
| <span data-ttu-id="8ae1e-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ae1e-120">Syntax</span></span>            | [<span data-ttu-id="8ae1e-121">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="8ae1e-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="8ae1e-122">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="8ae1e-122">Implementations</span></span>

-   [<span data-ttu-id="8ae1e-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8ae1e-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8ae1e-124">**Adam**</span><span class="sxs-lookup"><span data-stu-id="8ae1e-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8ae1e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8ae1e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8ae1e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8ae1e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8ae1e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8ae1e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8ae1e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8ae1e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8ae1e-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8ae1e-129">Windows Server 2003</span></span>



| <span data-ttu-id="8ae1e-130">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8ae1e-130">Entry</span></span> | <span data-ttu-id="8ae1e-131">Wert</span><span class="sxs-lookup"><span data-stu-id="8ae1e-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="8ae1e-132">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8ae1e-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8ae1e-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ae1e-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8ae1e-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ae1e-134">System-Only</span></span>            | <span data-ttu-id="8ae1e-135">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-135">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-136">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8ae1e-136">Is-Single-Valued</span></span>       | <span data-ttu-id="8ae1e-137">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ae1e-137">True</span></span>                                                              |
| <span data-ttu-id="8ae1e-138">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8ae1e-138">Is Indexed</span></span>             | <span data-ttu-id="8ae1e-139">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-139">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-140">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8ae1e-140">In Global Catalog</span></span>      | <span data-ttu-id="8ae1e-141">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-141">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8ae1e-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ae1e-143">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8ae1e-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="8ae1e-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ae1e-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="8ae1e-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ae1e-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="8ae1e-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ae1e-146">Search-Flags</span></span>           | <span data-ttu-id="8ae1e-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ae1e-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="8ae1e-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ae1e-148">System-Flags</span></span>           | <span data-ttu-id="8ae1e-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ae1e-149">0x00000010</span></span>                                                        |
| <span data-ttu-id="8ae1e-150">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8ae1e-150">Classes used in</span></span>        | [<span data-ttu-id="8ae1e-151">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="8ae1e-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8ae1e-152">Adam</span><span class="sxs-lookup"><span data-stu-id="8ae1e-152">ADAM</span></span>



| <span data-ttu-id="8ae1e-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8ae1e-153">Entry</span></span> | <span data-ttu-id="8ae1e-154">Wert</span><span class="sxs-lookup"><span data-stu-id="8ae1e-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="8ae1e-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8ae1e-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8ae1e-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ae1e-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8ae1e-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ae1e-157">System-Only</span></span>            | <span data-ttu-id="8ae1e-158">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-158">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8ae1e-159">Is-Single-Valued</span></span>       | <span data-ttu-id="8ae1e-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ae1e-160">True</span></span>                                                              |
| <span data-ttu-id="8ae1e-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8ae1e-161">Is Indexed</span></span>             | <span data-ttu-id="8ae1e-162">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-162">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8ae1e-163">In Global Catalog</span></span>      | <span data-ttu-id="8ae1e-164">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-164">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8ae1e-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ae1e-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8ae1e-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="8ae1e-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ae1e-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="8ae1e-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ae1e-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="8ae1e-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ae1e-169">Search-Flags</span></span>           | <span data-ttu-id="8ae1e-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ae1e-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="8ae1e-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ae1e-171">System-Flags</span></span>           | <span data-ttu-id="8ae1e-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ae1e-172">0x00000010</span></span>                                                        |
| <span data-ttu-id="8ae1e-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8ae1e-173">Classes used in</span></span>        | [<span data-ttu-id="8ae1e-174">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="8ae1e-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8ae1e-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8ae1e-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8ae1e-176">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8ae1e-176">Entry</span></span> | <span data-ttu-id="8ae1e-177">Wert</span><span class="sxs-lookup"><span data-stu-id="8ae1e-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="8ae1e-178">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8ae1e-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8ae1e-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ae1e-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8ae1e-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ae1e-180">System-Only</span></span>            | <span data-ttu-id="8ae1e-181">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-181">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-182">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8ae1e-182">Is-Single-Valued</span></span>       | <span data-ttu-id="8ae1e-183">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ae1e-183">True</span></span>                                                              |
| <span data-ttu-id="8ae1e-184">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8ae1e-184">Is Indexed</span></span>             | <span data-ttu-id="8ae1e-185">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-185">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-186">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8ae1e-186">In Global Catalog</span></span>      | <span data-ttu-id="8ae1e-187">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-187">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8ae1e-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ae1e-189">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8ae1e-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="8ae1e-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ae1e-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="8ae1e-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ae1e-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="8ae1e-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ae1e-192">Search-Flags</span></span>           | <span data-ttu-id="8ae1e-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ae1e-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="8ae1e-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ae1e-194">System-Flags</span></span>           | <span data-ttu-id="8ae1e-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ae1e-195">0x00000010</span></span>                                                        |
| <span data-ttu-id="8ae1e-196">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8ae1e-196">Classes used in</span></span>        | [<span data-ttu-id="8ae1e-197">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="8ae1e-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8ae1e-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ae1e-198">Windows Server 2008</span></span>



| <span data-ttu-id="8ae1e-199">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8ae1e-199">Entry</span></span> | <span data-ttu-id="8ae1e-200">Wert</span><span class="sxs-lookup"><span data-stu-id="8ae1e-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="8ae1e-201">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8ae1e-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8ae1e-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ae1e-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8ae1e-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ae1e-203">System-Only</span></span>            | <span data-ttu-id="8ae1e-204">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-204">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8ae1e-205">Is-Single-Valued</span></span>       | <span data-ttu-id="8ae1e-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ae1e-206">True</span></span>                                                              |
| <span data-ttu-id="8ae1e-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8ae1e-207">Is Indexed</span></span>             | <span data-ttu-id="8ae1e-208">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-208">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8ae1e-209">In Global Catalog</span></span>      | <span data-ttu-id="8ae1e-210">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-210">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8ae1e-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ae1e-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8ae1e-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="8ae1e-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ae1e-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="8ae1e-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ae1e-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="8ae1e-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ae1e-215">Search-Flags</span></span>           | <span data-ttu-id="8ae1e-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ae1e-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="8ae1e-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ae1e-217">System-Flags</span></span>           | <span data-ttu-id="8ae1e-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ae1e-218">0x00000010</span></span>                                                        |
| <span data-ttu-id="8ae1e-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8ae1e-219">Classes used in</span></span>        | [<span data-ttu-id="8ae1e-220">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="8ae1e-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8ae1e-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8ae1e-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8ae1e-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8ae1e-222">Entry</span></span> | <span data-ttu-id="8ae1e-223">Wert</span><span class="sxs-lookup"><span data-stu-id="8ae1e-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="8ae1e-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8ae1e-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8ae1e-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ae1e-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8ae1e-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ae1e-226">System-Only</span></span>            | <span data-ttu-id="8ae1e-227">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-227">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-228">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8ae1e-228">Is-Single-Valued</span></span>       | <span data-ttu-id="8ae1e-229">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ae1e-229">True</span></span>                                                              |
| <span data-ttu-id="8ae1e-230">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8ae1e-230">Is Indexed</span></span>             | <span data-ttu-id="8ae1e-231">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-231">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-232">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8ae1e-232">In Global Catalog</span></span>      | <span data-ttu-id="8ae1e-233">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-233">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8ae1e-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ae1e-235">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8ae1e-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="8ae1e-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ae1e-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="8ae1e-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ae1e-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="8ae1e-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ae1e-238">Search-Flags</span></span>           | <span data-ttu-id="8ae1e-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ae1e-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="8ae1e-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ae1e-240">System-Flags</span></span>           | <span data-ttu-id="8ae1e-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ae1e-241">0x00000010</span></span>                                                        |
| <span data-ttu-id="8ae1e-242">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8ae1e-242">Classes used in</span></span>        | [<span data-ttu-id="8ae1e-243">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="8ae1e-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8ae1e-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8ae1e-244">Windows Server 2012</span></span>



| <span data-ttu-id="8ae1e-245">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8ae1e-245">Entry</span></span> | <span data-ttu-id="8ae1e-246">Wert</span><span class="sxs-lookup"><span data-stu-id="8ae1e-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="8ae1e-247">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8ae1e-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8ae1e-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8ae1e-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8ae1e-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="8ae1e-249">System-Only</span></span>            | <span data-ttu-id="8ae1e-250">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-250">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-251">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8ae1e-251">Is-Single-Valued</span></span>       | <span data-ttu-id="8ae1e-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="8ae1e-252">True</span></span>                                                              |
| <span data-ttu-id="8ae1e-253">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8ae1e-253">Is Indexed</span></span>             | <span data-ttu-id="8ae1e-254">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-254">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-255">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8ae1e-255">In Global Catalog</span></span>      | <span data-ttu-id="8ae1e-256">False</span><span class="sxs-lookup"><span data-stu-id="8ae1e-256">False</span></span>                                                             |
| <span data-ttu-id="8ae1e-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8ae1e-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="8ae1e-258">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8ae1e-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="8ae1e-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8ae1e-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="8ae1e-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8ae1e-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="8ae1e-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8ae1e-261">Search-Flags</span></span>           | <span data-ttu-id="8ae1e-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8ae1e-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="8ae1e-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8ae1e-263">System-Flags</span></span>           | <span data-ttu-id="8ae1e-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8ae1e-264">0x00000010</span></span>                                                        |
| <span data-ttu-id="8ae1e-265">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8ae1e-265">Classes used in</span></span>        | [<span data-ttu-id="8ae1e-266">**ms-DS-Quota-Container**</span><span class="sxs-lookup"><span data-stu-id="8ae1e-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





