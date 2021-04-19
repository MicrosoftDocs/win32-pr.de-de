---
title: ms-DS-executescriptpassword-Attribut
description: Wird während der Domänen Umbenennung verwendet. Dieser Wert kann nicht mit LDAP geschrieben oder aus diesem gelesen werden.
ms.assetid: 381c3676-0a11-4e53-8093-f04dbf156250
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-DS-executescriptpassword-Attributs
- AD-Schema des msDS-executescriptpassword-Attributs
topic_type:
- apiref
api_name:
- ms-DS-ExecuteScriptPassword
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f01ebb231404188235236442df1d4916814f0636
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346366"
---
# <a name="ms-ds-executescriptpassword-attribute"></a><span data-ttu-id="f5911-106">ms-DS-executescriptpassword-Attribut</span><span class="sxs-lookup"><span data-stu-id="f5911-106">ms-DS-ExecuteScriptPassword attribute</span></span>

<span data-ttu-id="f5911-107">Wird während der Domänen Umbenennung verwendet.</span><span class="sxs-lookup"><span data-stu-id="f5911-107">Used during domain rename.</span></span> <span data-ttu-id="f5911-108">Dieser Wert kann nicht mit LDAP geschrieben oder aus diesem gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="f5911-108">This value cannot be written to or read from by using LDAP.</span></span>



| <span data-ttu-id="f5911-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f5911-109">Entry</span></span> | <span data-ttu-id="f5911-110">Wert</span><span class="sxs-lookup"><span data-stu-id="f5911-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="f5911-111">CN</span><span class="sxs-lookup"><span data-stu-id="f5911-111">CN</span></span>                | <span data-ttu-id="f5911-112">ms-DS-executescriptpassword</span><span class="sxs-lookup"><span data-stu-id="f5911-112">ms-DS-ExecuteScriptPassword</span></span>                           |
| <span data-ttu-id="f5911-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f5911-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f5911-114">MSDS-executescriptpassword</span><span class="sxs-lookup"><span data-stu-id="f5911-114">msDS-ExecuteScriptPassword</span></span>                            |
| <span data-ttu-id="f5911-115">Size</span><span class="sxs-lookup"><span data-stu-id="f5911-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="f5911-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f5911-116">Update Privilege</span></span>  | <span data-ttu-id="f5911-117">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f5911-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="f5911-118">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f5911-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="f5911-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f5911-119">Attribute-Id</span></span>      | <span data-ttu-id="f5911-120">1.2.840.113556.1.4.1783</span><span class="sxs-lookup"><span data-stu-id="f5911-120">1.2.840.113556.1.4.1783</span></span>                               |
| <span data-ttu-id="f5911-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f5911-121">System-Id-Guid</span></span>    | <span data-ttu-id="f5911-122">9d054a5a-D187-46c1-9d85-42dfc44a56dd</span><span class="sxs-lookup"><span data-stu-id="f5911-122">9d054a5a-d187-46c1-9d85-42dfc44a56dd</span></span>                  |
| <span data-ttu-id="f5911-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5911-123">Syntax</span></span>            | [<span data-ttu-id="f5911-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="f5911-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="f5911-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f5911-125">Implementations</span></span>

-   [<span data-ttu-id="f5911-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f5911-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f5911-127">**Adam**</span><span class="sxs-lookup"><span data-stu-id="f5911-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f5911-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f5911-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f5911-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f5911-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f5911-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f5911-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f5911-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f5911-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f5911-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f5911-132">Windows Server 2003</span></span>



| <span data-ttu-id="f5911-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f5911-133">Entry</span></span> | <span data-ttu-id="f5911-134">Wert</span><span class="sxs-lookup"><span data-stu-id="f5911-134">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f5911-135">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f5911-135">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f5911-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5911-136">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f5911-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5911-137">System-Only</span></span>            | <span data-ttu-id="f5911-138">Richtig</span><span class="sxs-lookup"><span data-stu-id="f5911-138">True</span></span>                                                          |
| <span data-ttu-id="f5911-139">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f5911-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f5911-140">Richtig</span><span class="sxs-lookup"><span data-stu-id="f5911-140">True</span></span>                                                          |
| <span data-ttu-id="f5911-141">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f5911-141">Is Indexed</span></span>             | <span data-ttu-id="f5911-142">False</span><span class="sxs-lookup"><span data-stu-id="f5911-142">False</span></span>                                                         |
| <span data-ttu-id="f5911-143">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f5911-143">In Global Catalog</span></span>      | <span data-ttu-id="f5911-144">False</span><span class="sxs-lookup"><span data-stu-id="f5911-144">False</span></span>                                                         |
| <span data-ttu-id="f5911-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5911-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5911-146">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f5911-146">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f5911-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5911-147">Range-Lower</span></span>            | <span data-ttu-id="f5911-148">0</span><span class="sxs-lookup"><span data-stu-id="f5911-148">0</span></span>                                                             |
| <span data-ttu-id="f5911-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5911-149">Range-Upper</span></span>            | <span data-ttu-id="f5911-150">64</span><span class="sxs-lookup"><span data-stu-id="f5911-150">64</span></span>                                                            |
| <span data-ttu-id="f5911-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5911-151">Search-Flags</span></span>           | <span data-ttu-id="f5911-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5911-152">0x00000000</span></span>                                                    |
| <span data-ttu-id="f5911-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5911-153">System-Flags</span></span>           | <span data-ttu-id="f5911-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f5911-154">0x00000011</span></span>                                                    |
| <span data-ttu-id="f5911-155">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f5911-155">Classes used in</span></span>        | [<span data-ttu-id="f5911-156">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="f5911-156">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f5911-157">Adam</span><span class="sxs-lookup"><span data-stu-id="f5911-157">ADAM</span></span>



| <span data-ttu-id="f5911-158">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f5911-158">Entry</span></span> | <span data-ttu-id="f5911-159">Wert</span><span class="sxs-lookup"><span data-stu-id="f5911-159">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f5911-160">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f5911-160">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f5911-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5911-161">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f5911-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5911-162">System-Only</span></span>            | <span data-ttu-id="f5911-163">Richtig</span><span class="sxs-lookup"><span data-stu-id="f5911-163">True</span></span>                                                          |
| <span data-ttu-id="f5911-164">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f5911-164">Is-Single-Valued</span></span>       | <span data-ttu-id="f5911-165">Richtig</span><span class="sxs-lookup"><span data-stu-id="f5911-165">True</span></span>                                                          |
| <span data-ttu-id="f5911-166">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f5911-166">Is Indexed</span></span>             | <span data-ttu-id="f5911-167">False</span><span class="sxs-lookup"><span data-stu-id="f5911-167">False</span></span>                                                         |
| <span data-ttu-id="f5911-168">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f5911-168">In Global Catalog</span></span>      | <span data-ttu-id="f5911-169">False</span><span class="sxs-lookup"><span data-stu-id="f5911-169">False</span></span>                                                         |
| <span data-ttu-id="f5911-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5911-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5911-171">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f5911-171">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f5911-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5911-172">Range-Lower</span></span>            | <span data-ttu-id="f5911-173">0</span><span class="sxs-lookup"><span data-stu-id="f5911-173">0</span></span>                                                             |
| <span data-ttu-id="f5911-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5911-174">Range-Upper</span></span>            | <span data-ttu-id="f5911-175">64</span><span class="sxs-lookup"><span data-stu-id="f5911-175">64</span></span>                                                            |
| <span data-ttu-id="f5911-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5911-176">Search-Flags</span></span>           | <span data-ttu-id="f5911-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5911-177">0x00000000</span></span>                                                    |
| <span data-ttu-id="f5911-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5911-178">System-Flags</span></span>           | <span data-ttu-id="f5911-179">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f5911-179">0x00000011</span></span>                                                    |
| <span data-ttu-id="f5911-180">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f5911-180">Classes used in</span></span>        | [<span data-ttu-id="f5911-181">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="f5911-181">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f5911-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f5911-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f5911-183">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f5911-183">Entry</span></span> | <span data-ttu-id="f5911-184">Wert</span><span class="sxs-lookup"><span data-stu-id="f5911-184">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f5911-185">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f5911-185">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f5911-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5911-186">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f5911-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5911-187">System-Only</span></span>            | <span data-ttu-id="f5911-188">Richtig</span><span class="sxs-lookup"><span data-stu-id="f5911-188">True</span></span>                                                          |
| <span data-ttu-id="f5911-189">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f5911-189">Is-Single-Valued</span></span>       | <span data-ttu-id="f5911-190">Richtig</span><span class="sxs-lookup"><span data-stu-id="f5911-190">True</span></span>                                                          |
| <span data-ttu-id="f5911-191">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f5911-191">Is Indexed</span></span>             | <span data-ttu-id="f5911-192">False</span><span class="sxs-lookup"><span data-stu-id="f5911-192">False</span></span>                                                         |
| <span data-ttu-id="f5911-193">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f5911-193">In Global Catalog</span></span>      | <span data-ttu-id="f5911-194">False</span><span class="sxs-lookup"><span data-stu-id="f5911-194">False</span></span>                                                         |
| <span data-ttu-id="f5911-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5911-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5911-196">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f5911-196">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f5911-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5911-197">Range-Lower</span></span>            | <span data-ttu-id="f5911-198">0</span><span class="sxs-lookup"><span data-stu-id="f5911-198">0</span></span>                                                             |
| <span data-ttu-id="f5911-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5911-199">Range-Upper</span></span>            | <span data-ttu-id="f5911-200">64</span><span class="sxs-lookup"><span data-stu-id="f5911-200">64</span></span>                                                            |
| <span data-ttu-id="f5911-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5911-201">Search-Flags</span></span>           | <span data-ttu-id="f5911-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5911-202">0x00000000</span></span>                                                    |
| <span data-ttu-id="f5911-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5911-203">System-Flags</span></span>           | <span data-ttu-id="f5911-204">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f5911-204">0x00000011</span></span>                                                    |
| <span data-ttu-id="f5911-205">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f5911-205">Classes used in</span></span>        | [<span data-ttu-id="f5911-206">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="f5911-206">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f5911-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5911-207">Windows Server 2008</span></span>



| <span data-ttu-id="f5911-208">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f5911-208">Entry</span></span> | <span data-ttu-id="f5911-209">Wert</span><span class="sxs-lookup"><span data-stu-id="f5911-209">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5911-210">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f5911-210">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="f5911-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5911-211">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="f5911-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5911-212">System-Only</span></span>            | <span data-ttu-id="f5911-213">Richtig</span><span class="sxs-lookup"><span data-stu-id="f5911-213">True</span></span>                                                                                                    |
| <span data-ttu-id="f5911-214">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f5911-214">Is-Single-Valued</span></span>       | <span data-ttu-id="f5911-215">Richtig</span><span class="sxs-lookup"><span data-stu-id="f5911-215">True</span></span>                                                                                                    |
| <span data-ttu-id="f5911-216">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f5911-216">Is Indexed</span></span>             | <span data-ttu-id="f5911-217">False</span><span class="sxs-lookup"><span data-stu-id="f5911-217">False</span></span>                                                                                                   |
| <span data-ttu-id="f5911-218">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f5911-218">In Global Catalog</span></span>      | <span data-ttu-id="f5911-219">False</span><span class="sxs-lookup"><span data-stu-id="f5911-219">False</span></span>                                                                                                   |
| <span data-ttu-id="f5911-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5911-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5911-221">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f5911-221">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="f5911-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5911-222">Range-Lower</span></span>            | <span data-ttu-id="f5911-223">0</span><span class="sxs-lookup"><span data-stu-id="f5911-223">0</span></span>                                                                                                       |
| <span data-ttu-id="f5911-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5911-224">Range-Upper</span></span>            | <span data-ttu-id="f5911-225">64</span><span class="sxs-lookup"><span data-stu-id="f5911-225">64</span></span>                                                                                                      |
| <span data-ttu-id="f5911-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5911-226">Search-Flags</span></span>           | <span data-ttu-id="f5911-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5911-227">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="f5911-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5911-228">System-Flags</span></span>           | <span data-ttu-id="f5911-229">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f5911-229">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="f5911-230">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f5911-230">Classes used in</span></span>        | [<span data-ttu-id="f5911-231">**Computer**</span><span class="sxs-lookup"><span data-stu-id="f5911-231">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="f5911-232">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="f5911-232">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f5911-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f5911-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f5911-234">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f5911-234">Entry</span></span> | <span data-ttu-id="f5911-235">Wert</span><span class="sxs-lookup"><span data-stu-id="f5911-235">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5911-236">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f5911-236">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="f5911-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5911-237">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="f5911-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5911-238">System-Only</span></span>            | <span data-ttu-id="f5911-239">Richtig</span><span class="sxs-lookup"><span data-stu-id="f5911-239">True</span></span>                                                                                                    |
| <span data-ttu-id="f5911-240">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f5911-240">Is-Single-Valued</span></span>       | <span data-ttu-id="f5911-241">Richtig</span><span class="sxs-lookup"><span data-stu-id="f5911-241">True</span></span>                                                                                                    |
| <span data-ttu-id="f5911-242">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f5911-242">Is Indexed</span></span>             | <span data-ttu-id="f5911-243">False</span><span class="sxs-lookup"><span data-stu-id="f5911-243">False</span></span>                                                                                                   |
| <span data-ttu-id="f5911-244">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f5911-244">In Global Catalog</span></span>      | <span data-ttu-id="f5911-245">False</span><span class="sxs-lookup"><span data-stu-id="f5911-245">False</span></span>                                                                                                   |
| <span data-ttu-id="f5911-246">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5911-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5911-247">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f5911-247">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="f5911-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5911-248">Range-Lower</span></span>            | <span data-ttu-id="f5911-249">0</span><span class="sxs-lookup"><span data-stu-id="f5911-249">0</span></span>                                                                                                       |
| <span data-ttu-id="f5911-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5911-250">Range-Upper</span></span>            | <span data-ttu-id="f5911-251">64</span><span class="sxs-lookup"><span data-stu-id="f5911-251">64</span></span>                                                                                                      |
| <span data-ttu-id="f5911-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5911-252">Search-Flags</span></span>           | <span data-ttu-id="f5911-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5911-253">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="f5911-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5911-254">System-Flags</span></span>           | <span data-ttu-id="f5911-255">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f5911-255">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="f5911-256">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f5911-256">Classes used in</span></span>        | [<span data-ttu-id="f5911-257">**Computer**</span><span class="sxs-lookup"><span data-stu-id="f5911-257">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="f5911-258">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="f5911-258">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f5911-259">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f5911-259">Windows Server 2012</span></span>



| <span data-ttu-id="f5911-260">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f5911-260">Entry</span></span> | <span data-ttu-id="f5911-261">Wert</span><span class="sxs-lookup"><span data-stu-id="f5911-261">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5911-262">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f5911-262">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="f5911-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5911-263">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="f5911-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5911-264">System-Only</span></span>            | <span data-ttu-id="f5911-265">Richtig</span><span class="sxs-lookup"><span data-stu-id="f5911-265">True</span></span>                                                                                                    |
| <span data-ttu-id="f5911-266">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f5911-266">Is-Single-Valued</span></span>       | <span data-ttu-id="f5911-267">Richtig</span><span class="sxs-lookup"><span data-stu-id="f5911-267">True</span></span>                                                                                                    |
| <span data-ttu-id="f5911-268">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f5911-268">Is Indexed</span></span>             | <span data-ttu-id="f5911-269">False</span><span class="sxs-lookup"><span data-stu-id="f5911-269">False</span></span>                                                                                                   |
| <span data-ttu-id="f5911-270">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f5911-270">In Global Catalog</span></span>      | <span data-ttu-id="f5911-271">False</span><span class="sxs-lookup"><span data-stu-id="f5911-271">False</span></span>                                                                                                   |
| <span data-ttu-id="f5911-272">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5911-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5911-273">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f5911-273">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="f5911-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5911-274">Range-Lower</span></span>            | <span data-ttu-id="f5911-275">0</span><span class="sxs-lookup"><span data-stu-id="f5911-275">0</span></span>                                                                                                       |
| <span data-ttu-id="f5911-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5911-276">Range-Upper</span></span>            | <span data-ttu-id="f5911-277">64</span><span class="sxs-lookup"><span data-stu-id="f5911-277">64</span></span>                                                                                                      |
| <span data-ttu-id="f5911-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5911-278">Search-Flags</span></span>           | <span data-ttu-id="f5911-279">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5911-279">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="f5911-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5911-280">System-Flags</span></span>           | <span data-ttu-id="f5911-281">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f5911-281">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="f5911-282">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f5911-282">Classes used in</span></span>        | [<span data-ttu-id="f5911-283">**Computer**</span><span class="sxs-lookup"><span data-stu-id="f5911-283">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="f5911-284">**Cross-Ref-Container**</span><span class="sxs-lookup"><span data-stu-id="f5911-284">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





