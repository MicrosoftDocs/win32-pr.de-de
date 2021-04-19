---
title: ms-DS-User-Account-Control-berechnetes Attribut
description: die Berechnung von msDS-User-Account-Control ist ähnlich wie userAccountControl, aber der Wert des Attributs kann zusätzliche Bits enthalten, die nicht persistent sind.
ms.assetid: 4c635c04-8d2e-41b4-809c-58ce64271a02
ms.tgt_platform: multiple
keywords:
- "\"ms-DS-User-Account-Control-berechnetes Attribut AD Schema\""
- AD-Schema "msDS-User-Account-Control-berechnetes Attribut"
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Control-Computed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b5e9b047dd44d637b56cae8ded9e0991c46025
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346563"
---
# <a name="ms-ds-user-account-control-computed-attribute"></a><span data-ttu-id="df55d-105">ms-DS-User-Account-Control-berechnetes Attribut</span><span class="sxs-lookup"><span data-stu-id="df55d-105">ms-DS-User-Account-Control-Computed attribute</span></span>

<span data-ttu-id="df55d-106">die **Berechnung von msDS-User-Account-Control** ist ähnlich wie [**userAccountControl**](a-useraccountcontrol.md), aber der Wert des Attributs kann zusätzliche Bits enthalten, die nicht persistent sind.</span><span class="sxs-lookup"><span data-stu-id="df55d-106">**msDS-User-Account-Control-Computed** is much like [**userAccountControl**](a-useraccountcontrol.md), but the attribute's value can contain additional bits that are not persisted.</span></span> <span data-ttu-id="df55d-107">Die berechneten Bits umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="df55d-107">The computed bits include the following.</span></span>



| <span data-ttu-id="df55d-108">Wert</span><span class="sxs-lookup"><span data-stu-id="df55d-108">Value</span></span>                | <span data-ttu-id="df55d-109">Name (in IADs. h definiert)</span><span class="sxs-lookup"><span data-stu-id="df55d-109">Name (defined in Iads.h)</span></span>                     |
|----------------------|----------------------------------------------|
| <span data-ttu-id="df55d-110">0x0010</span><span class="sxs-lookup"><span data-stu-id="df55d-110">0x0010</span></span><br/>    | <span data-ttu-id="df55d-111">**UF- \_ Sperre**</span><span class="sxs-lookup"><span data-stu-id="df55d-111">**UF\_LOCKOUT**</span></span><br/>                   |
| <span data-ttu-id="df55d-112">0x800000</span><span class="sxs-lookup"><span data-stu-id="df55d-112">0x800000</span></span><br/>  | <span data-ttu-id="df55d-113">**\_Kennwort ist \_ abgelaufen.**</span><span class="sxs-lookup"><span data-stu-id="df55d-113">**UF\_PASSWORD\_EXPIRED**</span></span><br/>         |
| <span data-ttu-id="df55d-114">0x4000000</span><span class="sxs-lookup"><span data-stu-id="df55d-114">0x4000000</span></span><br/> | <span data-ttu-id="df55d-115">**\_Konto für partielle \_ geheimen Schlüssel \_**</span><span class="sxs-lookup"><span data-stu-id="df55d-115">**UF\_PARTIAL\_SECRETS\_ACCOUNT**</span></span><br/> |
| <span data-ttu-id="df55d-116">0x8000000</span><span class="sxs-lookup"><span data-stu-id="df55d-116">0x8000000</span></span><br/> | <span data-ttu-id="df55d-117">**UF \_ Verwenden von \_ AES- \_ Schlüsseln**</span><span class="sxs-lookup"><span data-stu-id="df55d-117">**UF\_USE\_AES\_KEYS**</span></span><br/>            |



 

<span data-ttu-id="df55d-118">Die vollständige Liste der Bits, die [**Benutzerkontensteuerung**](a-useraccountcontrol.md) und somit auch **msDS-User-Account-Control-berechnete** Elemente enthalten können, finden Sie auch auf der Referenzseite für die **Benutzerkontensteuerung** (zugeordnet über das [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) -Flag) oder auf den Referenzseiten der Netzwerkverwaltung für die [**Benutzer \_ Info \_ 1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="df55d-118">The full list of bits that [**User-Account-Control**](a-useraccountcontrol.md) and therefore **msDS-User-Account-Control-Computed** can also contain can be found in the **User-Account-Control** reference page (mapped through the [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) flagset) or on the network management reference pages for the [**user\_info\_1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) structure.</span></span>



| <span data-ttu-id="df55d-119">Eingabe</span><span class="sxs-lookup"><span data-stu-id="df55d-119">Entry</span></span> | <span data-ttu-id="df55d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="df55d-120">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="df55d-121">CN</span><span class="sxs-lookup"><span data-stu-id="df55d-121">CN</span></span>                | <span data-ttu-id="df55d-122">ms-DS-User-Account-Control-berechnet</span><span class="sxs-lookup"><span data-stu-id="df55d-122">ms-DS-User-Account-Control-Computed</span></span>  |
| <span data-ttu-id="df55d-123">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="df55d-123">Ldap-Display-Name</span></span> | <span data-ttu-id="df55d-124">msDS-User-Account-Control-berechnet</span><span class="sxs-lookup"><span data-stu-id="df55d-124">msDS-User-Account-Control-Computed</span></span>   |
| <span data-ttu-id="df55d-125">Size</span><span class="sxs-lookup"><span data-stu-id="df55d-125">Size</span></span>              | \-                                   |
| <span data-ttu-id="df55d-126">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="df55d-126">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="df55d-127">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="df55d-127">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="df55d-128">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="df55d-128">Attribute-Id</span></span>      | <span data-ttu-id="df55d-129">1.2.840.113556.1.4.1460</span><span class="sxs-lookup"><span data-stu-id="df55d-129">1.2.840.113556.1.4.1460</span></span>              |
| <span data-ttu-id="df55d-130">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="df55d-130">System-Id-Guid</span></span>    | <span data-ttu-id="df55d-131">2cc4b836-B63-4940-8d23-ea7acf 06af56</span><span class="sxs-lookup"><span data-stu-id="df55d-131">2cc4b836-b63f-4940-8d23-ea7acf06af56</span></span> |
| <span data-ttu-id="df55d-132">Syntax</span><span class="sxs-lookup"><span data-stu-id="df55d-132">Syntax</span></span>            | [<span data-ttu-id="df55d-133">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="df55d-133">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="df55d-134">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="df55d-134">Implementations</span></span>

-   [<span data-ttu-id="df55d-135">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="df55d-135">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="df55d-136">**Adam**</span><span class="sxs-lookup"><span data-stu-id="df55d-136">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="df55d-137">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="df55d-137">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="df55d-138">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="df55d-138">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="df55d-139">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="df55d-139">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="df55d-140">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="df55d-140">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="df55d-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="df55d-141">Windows Server 2003</span></span>



| <span data-ttu-id="df55d-142">Eingabe</span><span class="sxs-lookup"><span data-stu-id="df55d-142">Entry</span></span> | <span data-ttu-id="df55d-143">Wert</span><span class="sxs-lookup"><span data-stu-id="df55d-143">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="df55d-144">Link-ID</span><span class="sxs-lookup"><span data-stu-id="df55d-144">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="df55d-145">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df55d-145">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="df55d-146">System-Only</span><span class="sxs-lookup"><span data-stu-id="df55d-146">System-Only</span></span>            | <span data-ttu-id="df55d-147">False</span><span class="sxs-lookup"><span data-stu-id="df55d-147">False</span></span>                             |
| <span data-ttu-id="df55d-148">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="df55d-148">Is-Single-Valued</span></span>       | <span data-ttu-id="df55d-149">Richtig</span><span class="sxs-lookup"><span data-stu-id="df55d-149">True</span></span>                              |
| <span data-ttu-id="df55d-150">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="df55d-150">Is Indexed</span></span>             | <span data-ttu-id="df55d-151">False</span><span class="sxs-lookup"><span data-stu-id="df55d-151">False</span></span>                             |
| <span data-ttu-id="df55d-152">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="df55d-152">In Global Catalog</span></span>      | <span data-ttu-id="df55d-153">False</span><span class="sxs-lookup"><span data-stu-id="df55d-153">False</span></span>                             |
| <span data-ttu-id="df55d-154">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df55d-154">NT-Security-Descriptor</span></span> | <span data-ttu-id="df55d-155">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="df55d-155">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="df55d-156">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df55d-156">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="df55d-157">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df55d-157">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="df55d-158">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df55d-158">Search-Flags</span></span>           | <span data-ttu-id="df55d-159">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df55d-159">0x00000000</span></span>                        |
| <span data-ttu-id="df55d-160">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df55d-160">System-Flags</span></span>           | <span data-ttu-id="df55d-161">0x00000014</span><span class="sxs-lookup"><span data-stu-id="df55d-161">0x00000014</span></span>                        |
| <span data-ttu-id="df55d-162">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="df55d-162">Classes used in</span></span>        | [<span data-ttu-id="df55d-163">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="df55d-163">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="df55d-164">Adam</span><span class="sxs-lookup"><span data-stu-id="df55d-164">ADAM</span></span>



| <span data-ttu-id="df55d-165">Eingabe</span><span class="sxs-lookup"><span data-stu-id="df55d-165">Entry</span></span> | <span data-ttu-id="df55d-166">Wert</span><span class="sxs-lookup"><span data-stu-id="df55d-166">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="df55d-167">Link-ID</span><span class="sxs-lookup"><span data-stu-id="df55d-167">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="df55d-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df55d-168">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="df55d-169">System-Only</span><span class="sxs-lookup"><span data-stu-id="df55d-169">System-Only</span></span>            | <span data-ttu-id="df55d-170">False</span><span class="sxs-lookup"><span data-stu-id="df55d-170">False</span></span>                                                             |
| <span data-ttu-id="df55d-171">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="df55d-171">Is-Single-Valued</span></span>       | <span data-ttu-id="df55d-172">Richtig</span><span class="sxs-lookup"><span data-stu-id="df55d-172">True</span></span>                                                              |
| <span data-ttu-id="df55d-173">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="df55d-173">Is Indexed</span></span>             | <span data-ttu-id="df55d-174">False</span><span class="sxs-lookup"><span data-stu-id="df55d-174">False</span></span>                                                             |
| <span data-ttu-id="df55d-175">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="df55d-175">In Global Catalog</span></span>      | <span data-ttu-id="df55d-176">False</span><span class="sxs-lookup"><span data-stu-id="df55d-176">False</span></span>                                                             |
| <span data-ttu-id="df55d-177">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df55d-177">NT-Security-Descriptor</span></span> | <span data-ttu-id="df55d-178">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="df55d-178">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="df55d-179">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df55d-179">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="df55d-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df55d-180">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="df55d-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df55d-181">Search-Flags</span></span>           | <span data-ttu-id="df55d-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df55d-182">0x00000000</span></span>                                                        |
| <span data-ttu-id="df55d-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df55d-183">System-Flags</span></span>           | <span data-ttu-id="df55d-184">0x00000014</span><span class="sxs-lookup"><span data-stu-id="df55d-184">0x00000014</span></span>                                                        |
| <span data-ttu-id="df55d-185">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="df55d-185">Classes used in</span></span>        | [<span data-ttu-id="df55d-186">**ms-DS-Bindable-Objekt**</span><span class="sxs-lookup"><span data-stu-id="df55d-186">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="df55d-187">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="df55d-187">Windows Server 2003 R2</span></span>



| <span data-ttu-id="df55d-188">Eingabe</span><span class="sxs-lookup"><span data-stu-id="df55d-188">Entry</span></span> | <span data-ttu-id="df55d-189">Wert</span><span class="sxs-lookup"><span data-stu-id="df55d-189">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="df55d-190">Link-ID</span><span class="sxs-lookup"><span data-stu-id="df55d-190">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="df55d-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df55d-191">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="df55d-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="df55d-192">System-Only</span></span>            | <span data-ttu-id="df55d-193">False</span><span class="sxs-lookup"><span data-stu-id="df55d-193">False</span></span>                             |
| <span data-ttu-id="df55d-194">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="df55d-194">Is-Single-Valued</span></span>       | <span data-ttu-id="df55d-195">Richtig</span><span class="sxs-lookup"><span data-stu-id="df55d-195">True</span></span>                              |
| <span data-ttu-id="df55d-196">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="df55d-196">Is Indexed</span></span>             | <span data-ttu-id="df55d-197">False</span><span class="sxs-lookup"><span data-stu-id="df55d-197">False</span></span>                             |
| <span data-ttu-id="df55d-198">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="df55d-198">In Global Catalog</span></span>      | <span data-ttu-id="df55d-199">False</span><span class="sxs-lookup"><span data-stu-id="df55d-199">False</span></span>                             |
| <span data-ttu-id="df55d-200">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df55d-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="df55d-201">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="df55d-201">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="df55d-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df55d-202">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="df55d-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df55d-203">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="df55d-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df55d-204">Search-Flags</span></span>           | <span data-ttu-id="df55d-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df55d-205">0x00000000</span></span>                        |
| <span data-ttu-id="df55d-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df55d-206">System-Flags</span></span>           | <span data-ttu-id="df55d-207">0x00000014</span><span class="sxs-lookup"><span data-stu-id="df55d-207">0x00000014</span></span>                        |
| <span data-ttu-id="df55d-208">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="df55d-208">Classes used in</span></span>        | [<span data-ttu-id="df55d-209">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="df55d-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="df55d-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df55d-210">Windows Server 2008</span></span>



| <span data-ttu-id="df55d-211">Eingabe</span><span class="sxs-lookup"><span data-stu-id="df55d-211">Entry</span></span> | <span data-ttu-id="df55d-212">Wert</span><span class="sxs-lookup"><span data-stu-id="df55d-212">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="df55d-213">Link-ID</span><span class="sxs-lookup"><span data-stu-id="df55d-213">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="df55d-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df55d-214">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="df55d-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="df55d-215">System-Only</span></span>            | <span data-ttu-id="df55d-216">False</span><span class="sxs-lookup"><span data-stu-id="df55d-216">False</span></span>                             |
| <span data-ttu-id="df55d-217">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="df55d-217">Is-Single-Valued</span></span>       | <span data-ttu-id="df55d-218">Richtig</span><span class="sxs-lookup"><span data-stu-id="df55d-218">True</span></span>                              |
| <span data-ttu-id="df55d-219">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="df55d-219">Is Indexed</span></span>             | <span data-ttu-id="df55d-220">False</span><span class="sxs-lookup"><span data-stu-id="df55d-220">False</span></span>                             |
| <span data-ttu-id="df55d-221">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="df55d-221">In Global Catalog</span></span>      | <span data-ttu-id="df55d-222">False</span><span class="sxs-lookup"><span data-stu-id="df55d-222">False</span></span>                             |
| <span data-ttu-id="df55d-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df55d-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="df55d-224">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="df55d-224">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="df55d-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df55d-225">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="df55d-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df55d-226">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="df55d-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df55d-227">Search-Flags</span></span>           | <span data-ttu-id="df55d-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df55d-228">0x00000000</span></span>                        |
| <span data-ttu-id="df55d-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df55d-229">System-Flags</span></span>           | <span data-ttu-id="df55d-230">0x00000014</span><span class="sxs-lookup"><span data-stu-id="df55d-230">0x00000014</span></span>                        |
| <span data-ttu-id="df55d-231">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="df55d-231">Classes used in</span></span>        | [<span data-ttu-id="df55d-232">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="df55d-232">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="df55d-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="df55d-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="df55d-234">Eingabe</span><span class="sxs-lookup"><span data-stu-id="df55d-234">Entry</span></span> | <span data-ttu-id="df55d-235">Wert</span><span class="sxs-lookup"><span data-stu-id="df55d-235">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="df55d-236">Link-ID</span><span class="sxs-lookup"><span data-stu-id="df55d-236">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="df55d-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df55d-237">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="df55d-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="df55d-238">System-Only</span></span>            | <span data-ttu-id="df55d-239">False</span><span class="sxs-lookup"><span data-stu-id="df55d-239">False</span></span>                             |
| <span data-ttu-id="df55d-240">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="df55d-240">Is-Single-Valued</span></span>       | <span data-ttu-id="df55d-241">Richtig</span><span class="sxs-lookup"><span data-stu-id="df55d-241">True</span></span>                              |
| <span data-ttu-id="df55d-242">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="df55d-242">Is Indexed</span></span>             | <span data-ttu-id="df55d-243">False</span><span class="sxs-lookup"><span data-stu-id="df55d-243">False</span></span>                             |
| <span data-ttu-id="df55d-244">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="df55d-244">In Global Catalog</span></span>      | <span data-ttu-id="df55d-245">False</span><span class="sxs-lookup"><span data-stu-id="df55d-245">False</span></span>                             |
| <span data-ttu-id="df55d-246">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df55d-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="df55d-247">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="df55d-247">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="df55d-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df55d-248">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="df55d-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df55d-249">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="df55d-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df55d-250">Search-Flags</span></span>           | <span data-ttu-id="df55d-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df55d-251">0x00000000</span></span>                        |
| <span data-ttu-id="df55d-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df55d-252">System-Flags</span></span>           | <span data-ttu-id="df55d-253">0x00000014</span><span class="sxs-lookup"><span data-stu-id="df55d-253">0x00000014</span></span>                        |
| <span data-ttu-id="df55d-254">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="df55d-254">Classes used in</span></span>        | [<span data-ttu-id="df55d-255">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="df55d-255">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="df55d-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="df55d-256">Windows Server 2012</span></span>



| <span data-ttu-id="df55d-257">Eingabe</span><span class="sxs-lookup"><span data-stu-id="df55d-257">Entry</span></span> | <span data-ttu-id="df55d-258">Wert</span><span class="sxs-lookup"><span data-stu-id="df55d-258">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="df55d-259">Link-ID</span><span class="sxs-lookup"><span data-stu-id="df55d-259">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="df55d-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="df55d-260">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="df55d-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="df55d-261">System-Only</span></span>            | <span data-ttu-id="df55d-262">False</span><span class="sxs-lookup"><span data-stu-id="df55d-262">False</span></span>                             |
| <span data-ttu-id="df55d-263">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="df55d-263">Is-Single-Valued</span></span>       | <span data-ttu-id="df55d-264">Richtig</span><span class="sxs-lookup"><span data-stu-id="df55d-264">True</span></span>                              |
| <span data-ttu-id="df55d-265">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="df55d-265">Is Indexed</span></span>             | <span data-ttu-id="df55d-266">False</span><span class="sxs-lookup"><span data-stu-id="df55d-266">False</span></span>                             |
| <span data-ttu-id="df55d-267">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="df55d-267">In Global Catalog</span></span>      | <span data-ttu-id="df55d-268">False</span><span class="sxs-lookup"><span data-stu-id="df55d-268">False</span></span>                             |
| <span data-ttu-id="df55d-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="df55d-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="df55d-270">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="df55d-270">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="df55d-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="df55d-271">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="df55d-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="df55d-272">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="df55d-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="df55d-273">Search-Flags</span></span>           | <span data-ttu-id="df55d-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="df55d-274">0x00000000</span></span>                        |
| <span data-ttu-id="df55d-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="df55d-275">System-Flags</span></span>           | <span data-ttu-id="df55d-276">0x00000014</span><span class="sxs-lookup"><span data-stu-id="df55d-276">0x00000014</span></span>                        |
| <span data-ttu-id="df55d-277">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="df55d-277">Classes used in</span></span>        | [<span data-ttu-id="df55d-278">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="df55d-278">**User**</span></span>](c-user.md)<br/> |



 

