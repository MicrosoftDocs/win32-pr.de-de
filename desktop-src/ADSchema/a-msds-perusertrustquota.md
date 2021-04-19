---
title: MS-DS-pro-Benutzer-Trust-Quota-Attribut
description: Wird verwendet, um ein pro-Benutzer-Kontingent zum Erstellen von Trusted-Domain Objekten zu erzwingen, die vom neuen Steuerelement Zugriffsrecht, CREATE-Inbound-Forest-Trust, autorisiert werden.
ms.assetid: 3b198b24-5282-4d13-8d35-88f34c11ce94
ms.tgt_platform: multiple
keywords:
- AD-Schema für das "ms-DS-pro-User-Trust-Quota"-Attribut
- AD-Schema des msDS-perusertrustquota-Attributs
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3bd6ffcac01de8997f806e6aa8a8e3bd6afbb66
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342529"
---
# <a name="ms-ds-per-user-trust-quota-attribute"></a><span data-ttu-id="ded15-105">MS-DS-pro-Benutzer-Trust-Quota-Attribut</span><span class="sxs-lookup"><span data-stu-id="ded15-105">MS-DS-Per-User-Trust-Quota attribute</span></span>

<span data-ttu-id="ded15-106">Wird verwendet, um ein pro-Benutzer-Kontingent zum Erstellen von Trusted-Domain Objekten zu erzwingen, die vom neuen Steuerelement Zugriffsrecht, CREATE-Inbound-Forest-Trust, autorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ded15-106">Used to enforce a per-user quota for creating Trusted-Domain objects that are authorized by the new control access right, Create-Inbound-Forest-Trust.</span></span> <span data-ttu-id="ded15-107">Dieses Attribut schränkt die Anzahl der Trusted-Domain Objekte ein, die von einem einzelnen Benutzer ohne Administratorrechte erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="ded15-107">This attribute limits the number of Trusted-Domain objects that can be created by a single non-admin user.</span></span>



| <span data-ttu-id="ded15-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ded15-108">Entry</span></span> | <span data-ttu-id="ded15-109">Wert</span><span class="sxs-lookup"><span data-stu-id="ded15-109">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="ded15-110">CN</span><span class="sxs-lookup"><span data-stu-id="ded15-110">CN</span></span>                | <span data-ttu-id="ded15-111">MS-DS-pro Benutzer-Trust-Quota</span><span class="sxs-lookup"><span data-stu-id="ded15-111">MS-DS-Per-User-Trust-Quota</span></span>                |
| <span data-ttu-id="ded15-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ded15-112">Ldap-Display-Name</span></span> | <span data-ttu-id="ded15-113">MSDS-perusertrustquota</span><span class="sxs-lookup"><span data-stu-id="ded15-113">msDS-PerUserTrustQuota</span></span>                    |
| <span data-ttu-id="ded15-114">Size</span><span class="sxs-lookup"><span data-stu-id="ded15-114">Size</span></span>              | \-                                        |
| <span data-ttu-id="ded15-115">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ded15-115">Update Privilege</span></span>  | <span data-ttu-id="ded15-116">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="ded15-116">Domain administrator</span></span>                      |
| <span data-ttu-id="ded15-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="ded15-117">Update Frequency</span></span>  | <span data-ttu-id="ded15-118">Bei der Gesamtstruktur Erstellung und selten danach.</span><span class="sxs-lookup"><span data-stu-id="ded15-118">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="ded15-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ded15-119">Attribute-Id</span></span>      | <span data-ttu-id="ded15-120">1.2.840.113556.1.4.1788</span><span class="sxs-lookup"><span data-stu-id="ded15-120">1.2.840.113556.1.4.1788</span></span>                   |
| <span data-ttu-id="ded15-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ded15-121">System-Id-Guid</span></span>    | <span data-ttu-id="ded15-122">d161adf0-ca24-4993-a3aa-8b2c981302e8</span><span class="sxs-lookup"><span data-stu-id="ded15-122">d161adf0-ca24-4993-a3aa-8b2c981302e8</span></span>      |
| <span data-ttu-id="ded15-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="ded15-123">Syntax</span></span>            | [<span data-ttu-id="ded15-124">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="ded15-124">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="ded15-125">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ded15-125">Implementations</span></span>

-   [<span data-ttu-id="ded15-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ded15-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ded15-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ded15-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ded15-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ded15-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ded15-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ded15-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ded15-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ded15-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ded15-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ded15-131">Windows Server 2003</span></span>



| <span data-ttu-id="ded15-132">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ded15-132">Entry</span></span> | <span data-ttu-id="ded15-133">Wert</span><span class="sxs-lookup"><span data-stu-id="ded15-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ded15-134">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ded15-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ded15-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ded15-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ded15-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ded15-136">System-Only</span></span>            | <span data-ttu-id="ded15-137">False</span><span class="sxs-lookup"><span data-stu-id="ded15-137">False</span></span>                                        |
| <span data-ttu-id="ded15-138">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ded15-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ded15-139">Richtig</span><span class="sxs-lookup"><span data-stu-id="ded15-139">True</span></span>                                         |
| <span data-ttu-id="ded15-140">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ded15-140">Is Indexed</span></span>             | <span data-ttu-id="ded15-141">False</span><span class="sxs-lookup"><span data-stu-id="ded15-141">False</span></span>                                        |
| <span data-ttu-id="ded15-142">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ded15-142">In Global Catalog</span></span>      | <span data-ttu-id="ded15-143">False</span><span class="sxs-lookup"><span data-stu-id="ded15-143">False</span></span>                                        |
| <span data-ttu-id="ded15-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ded15-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ded15-145">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ded15-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ded15-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ded15-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ded15-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ded15-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ded15-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ded15-148">Search-Flags</span></span>           | <span data-ttu-id="ded15-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ded15-149">0x00000000</span></span>                                   |
| <span data-ttu-id="ded15-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ded15-150">System-Flags</span></span>           | <span data-ttu-id="ded15-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ded15-151">0x00000010</span></span>                                   |
| <span data-ttu-id="ded15-152">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ded15-152">Classes used in</span></span>        | [<span data-ttu-id="ded15-153">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="ded15-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ded15-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ded15-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ded15-155">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ded15-155">Entry</span></span> | <span data-ttu-id="ded15-156">Wert</span><span class="sxs-lookup"><span data-stu-id="ded15-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ded15-157">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ded15-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ded15-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ded15-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ded15-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ded15-159">System-Only</span></span>            | <span data-ttu-id="ded15-160">False</span><span class="sxs-lookup"><span data-stu-id="ded15-160">False</span></span>                                        |
| <span data-ttu-id="ded15-161">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ded15-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ded15-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="ded15-162">True</span></span>                                         |
| <span data-ttu-id="ded15-163">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ded15-163">Is Indexed</span></span>             | <span data-ttu-id="ded15-164">False</span><span class="sxs-lookup"><span data-stu-id="ded15-164">False</span></span>                                        |
| <span data-ttu-id="ded15-165">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ded15-165">In Global Catalog</span></span>      | <span data-ttu-id="ded15-166">False</span><span class="sxs-lookup"><span data-stu-id="ded15-166">False</span></span>                                        |
| <span data-ttu-id="ded15-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ded15-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ded15-168">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ded15-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ded15-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ded15-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ded15-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ded15-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ded15-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ded15-171">Search-Flags</span></span>           | <span data-ttu-id="ded15-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ded15-172">0x00000000</span></span>                                   |
| <span data-ttu-id="ded15-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ded15-173">System-Flags</span></span>           | <span data-ttu-id="ded15-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ded15-174">0x00000010</span></span>                                   |
| <span data-ttu-id="ded15-175">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ded15-175">Classes used in</span></span>        | [<span data-ttu-id="ded15-176">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="ded15-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ded15-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ded15-177">Windows Server 2008</span></span>



| <span data-ttu-id="ded15-178">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ded15-178">Entry</span></span> | <span data-ttu-id="ded15-179">Wert</span><span class="sxs-lookup"><span data-stu-id="ded15-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ded15-180">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ded15-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ded15-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ded15-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ded15-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ded15-182">System-Only</span></span>            | <span data-ttu-id="ded15-183">False</span><span class="sxs-lookup"><span data-stu-id="ded15-183">False</span></span>                                        |
| <span data-ttu-id="ded15-184">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ded15-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ded15-185">Richtig</span><span class="sxs-lookup"><span data-stu-id="ded15-185">True</span></span>                                         |
| <span data-ttu-id="ded15-186">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ded15-186">Is Indexed</span></span>             | <span data-ttu-id="ded15-187">False</span><span class="sxs-lookup"><span data-stu-id="ded15-187">False</span></span>                                        |
| <span data-ttu-id="ded15-188">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ded15-188">In Global Catalog</span></span>      | <span data-ttu-id="ded15-189">False</span><span class="sxs-lookup"><span data-stu-id="ded15-189">False</span></span>                                        |
| <span data-ttu-id="ded15-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ded15-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ded15-191">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ded15-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ded15-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ded15-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ded15-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ded15-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ded15-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ded15-194">Search-Flags</span></span>           | <span data-ttu-id="ded15-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ded15-195">0x00000000</span></span>                                   |
| <span data-ttu-id="ded15-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ded15-196">System-Flags</span></span>           | <span data-ttu-id="ded15-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ded15-197">0x00000010</span></span>                                   |
| <span data-ttu-id="ded15-198">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ded15-198">Classes used in</span></span>        | [<span data-ttu-id="ded15-199">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="ded15-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ded15-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ded15-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ded15-201">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ded15-201">Entry</span></span> | <span data-ttu-id="ded15-202">Wert</span><span class="sxs-lookup"><span data-stu-id="ded15-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ded15-203">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ded15-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ded15-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ded15-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ded15-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ded15-205">System-Only</span></span>            | <span data-ttu-id="ded15-206">False</span><span class="sxs-lookup"><span data-stu-id="ded15-206">False</span></span>                                        |
| <span data-ttu-id="ded15-207">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ded15-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ded15-208">Richtig</span><span class="sxs-lookup"><span data-stu-id="ded15-208">True</span></span>                                         |
| <span data-ttu-id="ded15-209">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ded15-209">Is Indexed</span></span>             | <span data-ttu-id="ded15-210">False</span><span class="sxs-lookup"><span data-stu-id="ded15-210">False</span></span>                                        |
| <span data-ttu-id="ded15-211">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ded15-211">In Global Catalog</span></span>      | <span data-ttu-id="ded15-212">False</span><span class="sxs-lookup"><span data-stu-id="ded15-212">False</span></span>                                        |
| <span data-ttu-id="ded15-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ded15-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ded15-214">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ded15-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ded15-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ded15-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ded15-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ded15-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ded15-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ded15-217">Search-Flags</span></span>           | <span data-ttu-id="ded15-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ded15-218">0x00000000</span></span>                                   |
| <span data-ttu-id="ded15-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ded15-219">System-Flags</span></span>           | <span data-ttu-id="ded15-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ded15-220">0x00000010</span></span>                                   |
| <span data-ttu-id="ded15-221">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ded15-221">Classes used in</span></span>        | [<span data-ttu-id="ded15-222">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="ded15-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ded15-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ded15-223">Windows Server 2012</span></span>



| <span data-ttu-id="ded15-224">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ded15-224">Entry</span></span> | <span data-ttu-id="ded15-225">Wert</span><span class="sxs-lookup"><span data-stu-id="ded15-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ded15-226">Link-ID</span><span class="sxs-lookup"><span data-stu-id="ded15-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ded15-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ded15-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ded15-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ded15-228">System-Only</span></span>            | <span data-ttu-id="ded15-229">False</span><span class="sxs-lookup"><span data-stu-id="ded15-229">False</span></span>                                        |
| <span data-ttu-id="ded15-230">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="ded15-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ded15-231">Richtig</span><span class="sxs-lookup"><span data-stu-id="ded15-231">True</span></span>                                         |
| <span data-ttu-id="ded15-232">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="ded15-232">Is Indexed</span></span>             | <span data-ttu-id="ded15-233">False</span><span class="sxs-lookup"><span data-stu-id="ded15-233">False</span></span>                                        |
| <span data-ttu-id="ded15-234">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="ded15-234">In Global Catalog</span></span>      | <span data-ttu-id="ded15-235">False</span><span class="sxs-lookup"><span data-stu-id="ded15-235">False</span></span>                                        |
| <span data-ttu-id="ded15-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ded15-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ded15-237">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="ded15-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ded15-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ded15-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ded15-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ded15-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ded15-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ded15-240">Search-Flags</span></span>           | <span data-ttu-id="ded15-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ded15-241">0x00000000</span></span>                                   |
| <span data-ttu-id="ded15-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ded15-242">System-Flags</span></span>           | <span data-ttu-id="ded15-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ded15-243">0x00000010</span></span>                                   |
| <span data-ttu-id="ded15-244">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="ded15-244">Classes used in</span></span>        | [<span data-ttu-id="ded15-245">**Sam-Domäne**</span><span class="sxs-lookup"><span data-stu-id="ded15-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





