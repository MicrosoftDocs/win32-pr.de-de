---
title: ms-DS-supported-Encryption-Types-Attribut
description: Die Verschlüsselungsalgorithmen, die von Benutzer-, Computer-oder Vertrauens Konten unterstützt werden. Beachten Sie, dass der KDC diese Informationen beim Erstellen eines Dienst Tickets für dieses Konto verwendet.
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- von ms-DS unterstützte-Encryption-Types-Attribut AD-Schema
- adschema des msDS-supportedencryptiontypes-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab16959d1f1cd4405cb661a6026f3734a134f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346578"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a><span data-ttu-id="d66e4-105">ms-DS-supported-Encryption-Types-Attribut</span><span class="sxs-lookup"><span data-stu-id="d66e4-105">ms-DS-Supported-Encryption-Types attribute</span></span>

<span data-ttu-id="d66e4-106">Die Verschlüsselungsalgorithmen, die von Benutzer-, Computer-oder Vertrauens Konten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d66e4-106">The encryption algorithms supported by user, computer or trust accounts.</span></span>

> [!Note]  
> <span data-ttu-id="d66e4-107">Der KDC verwendet diese Informationen bei der Erstellung eines Dienst Tickets für dieses Konto.</span><span class="sxs-lookup"><span data-stu-id="d66e4-107">The KDC uses this information while generating a service ticket for this account.</span></span> <span data-ttu-id="d66e4-108">Dienste und Computer können dieses Attribut auf den jeweiligen Konten in Active Directory automatisch aktualisieren und benötigen daher Schreibzugriff auf dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="d66e4-108">Services and Computers can automatically update this attribute on their respective accounts in Active Directory, and therefore need write access to this attribute.</span></span>

 



| <span data-ttu-id="d66e4-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d66e4-109">Entry</span></span> | <span data-ttu-id="d66e4-110">Wert</span><span class="sxs-lookup"><span data-stu-id="d66e4-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d66e4-111">CN</span><span class="sxs-lookup"><span data-stu-id="d66e4-111">CN</span></span>                | <span data-ttu-id="d66e4-112">ms-DS-supported-Encryption-Types</span><span class="sxs-lookup"><span data-stu-id="d66e4-112">ms-DS-Supported-Encryption-Types</span></span>     |
| <span data-ttu-id="d66e4-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d66e4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d66e4-114">MSDS-supportedencryptiontypes</span><span class="sxs-lookup"><span data-stu-id="d66e4-114">msDS-SupportedEncryptionTypes</span></span>        |
| <span data-ttu-id="d66e4-115">Size</span><span class="sxs-lookup"><span data-stu-id="d66e4-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="d66e4-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d66e4-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="d66e4-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="d66e4-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="d66e4-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d66e4-118">Attribute-Id</span></span>      | <span data-ttu-id="d66e4-119">1.2.840.113556.1.4.1963</span><span class="sxs-lookup"><span data-stu-id="d66e4-119">1.2.840.113556.1.4.1963</span></span>              |
| <span data-ttu-id="d66e4-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d66e4-120">System-Id-Guid</span></span>    | <span data-ttu-id="d66e4-121">20119867-1d04-4ab7-9371-cfc3d5df0afd</span><span class="sxs-lookup"><span data-stu-id="d66e4-121">20119867-1d04-4ab7-9371-cfc3d5df0afd</span></span> |
| <span data-ttu-id="d66e4-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="d66e4-122">Syntax</span></span>            | [<span data-ttu-id="d66e4-123">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="d66e4-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="d66e4-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="d66e4-124">Implementations</span></span>

-   [<span data-ttu-id="d66e4-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d66e4-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d66e4-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d66e4-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d66e4-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d66e4-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="d66e4-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d66e4-128">Windows Server 2008</span></span>



| <span data-ttu-id="d66e4-129">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d66e4-129">Entry</span></span> | <span data-ttu-id="d66e4-130">Wert</span><span class="sxs-lookup"><span data-stu-id="d66e4-130">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d66e4-131">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d66e4-131">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="d66e4-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d66e4-132">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="d66e4-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="d66e4-133">System-Only</span></span>            | <span data-ttu-id="d66e4-134">False</span><span class="sxs-lookup"><span data-stu-id="d66e4-134">False</span></span>                                                                                  |
| <span data-ttu-id="d66e4-135">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d66e4-135">Is-Single-Valued</span></span>       | <span data-ttu-id="d66e4-136">Richtig</span><span class="sxs-lookup"><span data-stu-id="d66e4-136">True</span></span>                                                                                   |
| <span data-ttu-id="d66e4-137">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d66e4-137">Is Indexed</span></span>             | <span data-ttu-id="d66e4-138">False</span><span class="sxs-lookup"><span data-stu-id="d66e4-138">False</span></span>                                                                                  |
| <span data-ttu-id="d66e4-139">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d66e4-139">In Global Catalog</span></span>      | <span data-ttu-id="d66e4-140">False</span><span class="sxs-lookup"><span data-stu-id="d66e4-140">False</span></span>                                                                                  |
| <span data-ttu-id="d66e4-141">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d66e4-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="d66e4-142">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d66e4-142">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="d66e4-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d66e4-143">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="d66e4-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d66e4-144">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="d66e4-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d66e4-145">Search-Flags</span></span>           | <span data-ttu-id="d66e4-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d66e4-146">0x00000000</span></span>                                                                             |
| <span data-ttu-id="d66e4-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d66e4-147">System-Flags</span></span>           | <span data-ttu-id="d66e4-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d66e4-148">0x00000010</span></span>                                                                             |
| <span data-ttu-id="d66e4-149">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d66e4-149">Classes used in</span></span>        | [<span data-ttu-id="d66e4-150">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="d66e4-150">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="d66e4-151">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="d66e4-151">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d66e4-152">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d66e4-152">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d66e4-153">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d66e4-153">Entry</span></span> | <span data-ttu-id="d66e4-154">Wert</span><span class="sxs-lookup"><span data-stu-id="d66e4-154">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d66e4-155">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d66e4-155">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="d66e4-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d66e4-156">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="d66e4-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="d66e4-157">System-Only</span></span>            | <span data-ttu-id="d66e4-158">False</span><span class="sxs-lookup"><span data-stu-id="d66e4-158">False</span></span>                                                                                  |
| <span data-ttu-id="d66e4-159">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d66e4-159">Is-Single-Valued</span></span>       | <span data-ttu-id="d66e4-160">Richtig</span><span class="sxs-lookup"><span data-stu-id="d66e4-160">True</span></span>                                                                                   |
| <span data-ttu-id="d66e4-161">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d66e4-161">Is Indexed</span></span>             | <span data-ttu-id="d66e4-162">False</span><span class="sxs-lookup"><span data-stu-id="d66e4-162">False</span></span>                                                                                  |
| <span data-ttu-id="d66e4-163">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d66e4-163">In Global Catalog</span></span>      | <span data-ttu-id="d66e4-164">False</span><span class="sxs-lookup"><span data-stu-id="d66e4-164">False</span></span>                                                                                  |
| <span data-ttu-id="d66e4-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d66e4-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="d66e4-166">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d66e4-166">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="d66e4-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d66e4-167">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="d66e4-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d66e4-168">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="d66e4-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d66e4-169">Search-Flags</span></span>           | <span data-ttu-id="d66e4-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d66e4-170">0x00000000</span></span>                                                                             |
| <span data-ttu-id="d66e4-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d66e4-171">System-Flags</span></span>           | <span data-ttu-id="d66e4-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d66e4-172">0x00000010</span></span>                                                                             |
| <span data-ttu-id="d66e4-173">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d66e4-173">Classes used in</span></span>        | [<span data-ttu-id="d66e4-174">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="d66e4-174">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="d66e4-175">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="d66e4-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d66e4-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d66e4-176">Windows Server 2012</span></span>



| <span data-ttu-id="d66e4-177">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d66e4-177">Entry</span></span> | <span data-ttu-id="d66e4-178">Wert</span><span class="sxs-lookup"><span data-stu-id="d66e4-178">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d66e4-179">Link-ID</span><span class="sxs-lookup"><span data-stu-id="d66e4-179">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="d66e4-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d66e4-180">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="d66e4-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d66e4-181">System-Only</span></span>            | <span data-ttu-id="d66e4-182">False</span><span class="sxs-lookup"><span data-stu-id="d66e4-182">False</span></span>                                                                                  |
| <span data-ttu-id="d66e4-183">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="d66e4-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d66e4-184">Richtig</span><span class="sxs-lookup"><span data-stu-id="d66e4-184">True</span></span>                                                                                   |
| <span data-ttu-id="d66e4-185">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="d66e4-185">Is Indexed</span></span>             | <span data-ttu-id="d66e4-186">False</span><span class="sxs-lookup"><span data-stu-id="d66e4-186">False</span></span>                                                                                  |
| <span data-ttu-id="d66e4-187">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="d66e4-187">In Global Catalog</span></span>      | <span data-ttu-id="d66e4-188">False</span><span class="sxs-lookup"><span data-stu-id="d66e4-188">False</span></span>                                                                                  |
| <span data-ttu-id="d66e4-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d66e4-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d66e4-190">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="d66e4-190">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="d66e4-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d66e4-191">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="d66e4-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d66e4-192">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="d66e4-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d66e4-193">Search-Flags</span></span>           | <span data-ttu-id="d66e4-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d66e4-194">0x00000000</span></span>                                                                             |
| <span data-ttu-id="d66e4-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d66e4-195">System-Flags</span></span>           | <span data-ttu-id="d66e4-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d66e4-196">0x00000010</span></span>                                                                             |
| <span data-ttu-id="d66e4-197">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="d66e4-197">Classes used in</span></span>        | [<span data-ttu-id="d66e4-198">**Vertrauenswürdige Domäne**</span><span class="sxs-lookup"><span data-stu-id="d66e4-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="d66e4-199">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="d66e4-199">**User**</span></span>](c-user.md)<br/> |



 

 





