---
title: Sam-Account-Type-Attribut
description: Dieses Attribut enthält Informationen zu jedem Kontotyp Objekt.
ms.assetid: 00479b89-1d96-4ace-bbd8-053ca9e548b0
ms.tgt_platform: multiple
keywords:
- AD-Schema des Sam-Account-Type-Attributs
- "\"samAccountType\"-Attribut, AD-Schema"
topic_type:
- apiref
api_name:
- SAM-Account-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51de46dac0faabcc248159f7dcabafcd6060725
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957444"
---
# <a name="sam-account-type-attribute"></a><span data-ttu-id="483bd-105">Sam-Account-Type-Attribut</span><span class="sxs-lookup"><span data-stu-id="483bd-105">SAM-Account-Type attribute</span></span>

<span data-ttu-id="483bd-106">Dieses Attribut enthält Informationen zu jedem Kontotyp Objekt.</span><span class="sxs-lookup"><span data-stu-id="483bd-106">This attribute contains information about every account type object.</span></span> <span data-ttu-id="483bd-107">Sie können eine Liste von Konto Typen auflisten, oder Sie können die API zum Anzeigen von Informationen verwenden, um eine Liste zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="483bd-107">You can enumerate a list of account types or you can use the Display Information API to create a list.</span></span> <span data-ttu-id="483bd-108">Da Computer, normale Benutzerkonten und vertrauenswürdige Konten auch als Benutzer Objekte aufgelistet werden können, müssen die Werte für diese Konten ein zusammenhängender Bereich sein.</span><span class="sxs-lookup"><span data-stu-id="483bd-108">Because computers, normal user accounts, and trust accounts can also be enumerated as user objects, the values for these accounts must be a contiguous range.</span></span>

<span data-ttu-id="483bd-109">Die möglichen Werte für dieses Attribut lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="483bd-109">The possible values for this attribute are the following:</span></span>

-   <span data-ttu-id="483bd-110">Sam- \_ Domänen \_ Objekt 0x0</span><span class="sxs-lookup"><span data-stu-id="483bd-110">SAM\_DOMAIN\_OBJECT 0x0</span></span>
-   <span data-ttu-id="483bd-111">Sam- \_ Gruppen \_ Objekt 0x10000000</span><span class="sxs-lookup"><span data-stu-id="483bd-111">SAM\_GROUP\_OBJECT 0x10000000</span></span>
-   <span data-ttu-id="483bd-112">Sam \_ - \_ Sicherheits \_ Gruppen \_ Objekt 0x10000001</span><span class="sxs-lookup"><span data-stu-id="483bd-112">SAM\_NON\_SECURITY\_GROUP\_OBJECT 0x10000001</span></span>
-   <span data-ttu-id="483bd-113">Sam- \_ Alias \_ Objekt 0x20000000</span><span class="sxs-lookup"><span data-stu-id="483bd-113">SAM\_ALIAS\_OBJECT 0x20000000</span></span>
-   <span data-ttu-id="483bd-114">Sam \_ - \_ Alias Objekt der nicht Sicherheit \_ \_ 0x20000001</span><span class="sxs-lookup"><span data-stu-id="483bd-114">SAM\_NON\_SECURITY\_ALIAS\_OBJECT 0x20000001</span></span>
-   <span data-ttu-id="483bd-115">Sam- \_ Benutzer \_ Objekt 0x30000000</span><span class="sxs-lookup"><span data-stu-id="483bd-115">SAM\_USER\_OBJECT 0x30000000</span></span>
-   <span data-ttu-id="483bd-116">Sam \_ Normal \_ Benutzer \_ Konto 0x30000000</span><span class="sxs-lookup"><span data-stu-id="483bd-116">SAM\_NORMAL\_USER\_ACCOUNT 0x30000000</span></span>
-   <span data-ttu-id="483bd-117">Sam- \_ Computer \_ Konto 0x30000001</span><span class="sxs-lookup"><span data-stu-id="483bd-117">SAM\_MACHINE\_ACCOUNT 0x30000001</span></span>
-   <span data-ttu-id="483bd-118">Sam- \_ Vertrauensstellungs \_ Konto 0x30000002</span><span class="sxs-lookup"><span data-stu-id="483bd-118">SAM\_TRUST\_ACCOUNT 0x30000002</span></span>
-   <span data-ttu-id="483bd-119">Sam- \_ App- \_ Basis \_ Gruppe 0x40000000</span><span class="sxs-lookup"><span data-stu-id="483bd-119">SAM\_APP\_BASIC\_GROUP 0x40000000</span></span>
-   <span data-ttu-id="483bd-120">Sam- \_ App- \_ Abfrage \_ Gruppe 0x40000001</span><span class="sxs-lookup"><span data-stu-id="483bd-120">SAM\_APP\_QUERY\_GROUP 0x40000001</span></span>
-   <span data-ttu-id="483bd-121">Sam \_ - \_ Kontotyp \_ Max 0x7FFFFFFF</span><span class="sxs-lookup"><span data-stu-id="483bd-121">SAM\_ACCOUNT\_TYPE\_MAX 0x7fffffff</span></span>



| <span data-ttu-id="483bd-122">Eingabe</span><span class="sxs-lookup"><span data-stu-id="483bd-122">Entry</span></span> | <span data-ttu-id="483bd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="483bd-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="483bd-124">CN</span><span class="sxs-lookup"><span data-stu-id="483bd-124">CN</span></span>                | <span data-ttu-id="483bd-125">Sam-Account-Type</span><span class="sxs-lookup"><span data-stu-id="483bd-125">SAM-Account-Type</span></span>                                                |
| <span data-ttu-id="483bd-126">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="483bd-126">Ldap-Display-Name</span></span> | <span data-ttu-id="483bd-127">sAMAccountType</span><span class="sxs-lookup"><span data-stu-id="483bd-127">sAMAccountType</span></span>                                                  |
| <span data-ttu-id="483bd-128">Size</span><span class="sxs-lookup"><span data-stu-id="483bd-128">Size</span></span>              | \-                                                              |
| <span data-ttu-id="483bd-129">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="483bd-129">Update Privilege</span></span>  | <span data-ttu-id="483bd-130">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="483bd-130">This value is set by the system.</span></span>                                |
| <span data-ttu-id="483bd-131">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="483bd-131">Update Frequency</span></span>  | <span data-ttu-id="483bd-132">Dies wird vom Betriebssystem festgelegt, wenn das Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="483bd-132">This is set by the operating system when the object is created.</span></span> |
| <span data-ttu-id="483bd-133">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="483bd-133">Attribute-Id</span></span>      | <span data-ttu-id="483bd-134">1.2.840.113556.1.4.302</span><span class="sxs-lookup"><span data-stu-id="483bd-134">1.2.840.113556.1.4.302</span></span>                                          |
| <span data-ttu-id="483bd-135">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="483bd-135">System-Id-Guid</span></span>    | <span data-ttu-id="483bd-136">6e7b626c-64-Dienst-D0-afd2-00c04f 930c9</span><span class="sxs-lookup"><span data-stu-id="483bd-136">6e7b626c-64f2-11d0-afd2-00c04fd930c9</span></span>                            |
| <span data-ttu-id="483bd-137">Syntax</span><span class="sxs-lookup"><span data-stu-id="483bd-137">Syntax</span></span>            | [<span data-ttu-id="483bd-138">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="483bd-138">**Enumeration**</span></span>](s-enumeration.md)                            |



## <a name="implementations"></a><span data-ttu-id="483bd-139">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="483bd-139">Implementations</span></span>

-   [<span data-ttu-id="483bd-140">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="483bd-140">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="483bd-141">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="483bd-141">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="483bd-142">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="483bd-142">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="483bd-143">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="483bd-143">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="483bd-144">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="483bd-144">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="483bd-145">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="483bd-145">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="483bd-146">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="483bd-146">Windows 2000 Server</span></span>



| <span data-ttu-id="483bd-147">Eingabe</span><span class="sxs-lookup"><span data-stu-id="483bd-147">Entry</span></span> | <span data-ttu-id="483bd-148">Wert</span><span class="sxs-lookup"><span data-stu-id="483bd-148">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="483bd-149">Link-ID</span><span class="sxs-lookup"><span data-stu-id="483bd-149">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="483bd-150">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="483bd-150">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="483bd-151">System-Only</span><span class="sxs-lookup"><span data-stu-id="483bd-151">System-Only</span></span>            | <span data-ttu-id="483bd-152">False</span><span class="sxs-lookup"><span data-stu-id="483bd-152">False</span></span>                                                        |
| <span data-ttu-id="483bd-153">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="483bd-153">Is-Single-Valued</span></span>       | <span data-ttu-id="483bd-154">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-154">True</span></span>                                                         |
| <span data-ttu-id="483bd-155">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="483bd-155">Is Indexed</span></span>             | <span data-ttu-id="483bd-156">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-156">True</span></span>                                                         |
| <span data-ttu-id="483bd-157">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="483bd-157">In Global Catalog</span></span>      | <span data-ttu-id="483bd-158">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-158">True</span></span>                                                         |
| <span data-ttu-id="483bd-159">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="483bd-159">NT-Security-Descriptor</span></span> | <span data-ttu-id="483bd-160">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="483bd-160">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="483bd-161">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="483bd-161">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="483bd-162">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="483bd-162">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="483bd-163">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="483bd-163">Search-Flags</span></span>           | <span data-ttu-id="483bd-164">0x00000001</span><span class="sxs-lookup"><span data-stu-id="483bd-164">0x00000001</span></span>                                                   |
| <span data-ttu-id="483bd-165">System-Flags</span><span class="sxs-lookup"><span data-stu-id="483bd-165">System-Flags</span></span>           | <span data-ttu-id="483bd-166">0x00000012</span><span class="sxs-lookup"><span data-stu-id="483bd-166">0x00000012</span></span>                                                   |
| <span data-ttu-id="483bd-167">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="483bd-167">Classes used in</span></span>        | [<span data-ttu-id="483bd-168">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="483bd-168">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="483bd-169">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="483bd-169">Windows Server 2003</span></span>



| <span data-ttu-id="483bd-170">Eingabe</span><span class="sxs-lookup"><span data-stu-id="483bd-170">Entry</span></span> | <span data-ttu-id="483bd-171">Wert</span><span class="sxs-lookup"><span data-stu-id="483bd-171">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="483bd-172">Link-ID</span><span class="sxs-lookup"><span data-stu-id="483bd-172">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="483bd-173">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="483bd-173">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="483bd-174">System-Only</span><span class="sxs-lookup"><span data-stu-id="483bd-174">System-Only</span></span>            | <span data-ttu-id="483bd-175">False</span><span class="sxs-lookup"><span data-stu-id="483bd-175">False</span></span>                                                        |
| <span data-ttu-id="483bd-176">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="483bd-176">Is-Single-Valued</span></span>       | <span data-ttu-id="483bd-177">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-177">True</span></span>                                                         |
| <span data-ttu-id="483bd-178">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="483bd-178">Is Indexed</span></span>             | <span data-ttu-id="483bd-179">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-179">True</span></span>                                                         |
| <span data-ttu-id="483bd-180">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="483bd-180">In Global Catalog</span></span>      | <span data-ttu-id="483bd-181">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-181">True</span></span>                                                         |
| <span data-ttu-id="483bd-182">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="483bd-182">NT-Security-Descriptor</span></span> | <span data-ttu-id="483bd-183">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="483bd-183">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="483bd-184">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="483bd-184">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="483bd-185">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="483bd-185">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="483bd-186">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="483bd-186">Search-Flags</span></span>           | <span data-ttu-id="483bd-187">0x00000001</span><span class="sxs-lookup"><span data-stu-id="483bd-187">0x00000001</span></span>                                                   |
| <span data-ttu-id="483bd-188">System-Flags</span><span class="sxs-lookup"><span data-stu-id="483bd-188">System-Flags</span></span>           | <span data-ttu-id="483bd-189">0x00000012</span><span class="sxs-lookup"><span data-stu-id="483bd-189">0x00000012</span></span>                                                   |
| <span data-ttu-id="483bd-190">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="483bd-190">Classes used in</span></span>        | [<span data-ttu-id="483bd-191">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="483bd-191">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="483bd-192">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="483bd-192">Windows Server 2003 R2</span></span>



| <span data-ttu-id="483bd-193">Eingabe</span><span class="sxs-lookup"><span data-stu-id="483bd-193">Entry</span></span> | <span data-ttu-id="483bd-194">Wert</span><span class="sxs-lookup"><span data-stu-id="483bd-194">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="483bd-195">Link-ID</span><span class="sxs-lookup"><span data-stu-id="483bd-195">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="483bd-196">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="483bd-196">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="483bd-197">System-Only</span><span class="sxs-lookup"><span data-stu-id="483bd-197">System-Only</span></span>            | <span data-ttu-id="483bd-198">False</span><span class="sxs-lookup"><span data-stu-id="483bd-198">False</span></span>                                                        |
| <span data-ttu-id="483bd-199">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="483bd-199">Is-Single-Valued</span></span>       | <span data-ttu-id="483bd-200">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-200">True</span></span>                                                         |
| <span data-ttu-id="483bd-201">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="483bd-201">Is Indexed</span></span>             | <span data-ttu-id="483bd-202">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-202">True</span></span>                                                         |
| <span data-ttu-id="483bd-203">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="483bd-203">In Global Catalog</span></span>      | <span data-ttu-id="483bd-204">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-204">True</span></span>                                                         |
| <span data-ttu-id="483bd-205">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="483bd-205">NT-Security-Descriptor</span></span> | <span data-ttu-id="483bd-206">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="483bd-206">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="483bd-207">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="483bd-207">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="483bd-208">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="483bd-208">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="483bd-209">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="483bd-209">Search-Flags</span></span>           | <span data-ttu-id="483bd-210">0x00000001</span><span class="sxs-lookup"><span data-stu-id="483bd-210">0x00000001</span></span>                                                   |
| <span data-ttu-id="483bd-211">System-Flags</span><span class="sxs-lookup"><span data-stu-id="483bd-211">System-Flags</span></span>           | <span data-ttu-id="483bd-212">0x00000012</span><span class="sxs-lookup"><span data-stu-id="483bd-212">0x00000012</span></span>                                                   |
| <span data-ttu-id="483bd-213">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="483bd-213">Classes used in</span></span>        | [<span data-ttu-id="483bd-214">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="483bd-214">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="483bd-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="483bd-215">Windows Server 2008</span></span>



| <span data-ttu-id="483bd-216">Eingabe</span><span class="sxs-lookup"><span data-stu-id="483bd-216">Entry</span></span> | <span data-ttu-id="483bd-217">Wert</span><span class="sxs-lookup"><span data-stu-id="483bd-217">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="483bd-218">Link-ID</span><span class="sxs-lookup"><span data-stu-id="483bd-218">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="483bd-219">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="483bd-219">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="483bd-220">System-Only</span><span class="sxs-lookup"><span data-stu-id="483bd-220">System-Only</span></span>            | <span data-ttu-id="483bd-221">False</span><span class="sxs-lookup"><span data-stu-id="483bd-221">False</span></span>                                                        |
| <span data-ttu-id="483bd-222">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="483bd-222">Is-Single-Valued</span></span>       | <span data-ttu-id="483bd-223">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-223">True</span></span>                                                         |
| <span data-ttu-id="483bd-224">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="483bd-224">Is Indexed</span></span>             | <span data-ttu-id="483bd-225">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-225">True</span></span>                                                         |
| <span data-ttu-id="483bd-226">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="483bd-226">In Global Catalog</span></span>      | <span data-ttu-id="483bd-227">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-227">True</span></span>                                                         |
| <span data-ttu-id="483bd-228">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="483bd-228">NT-Security-Descriptor</span></span> | <span data-ttu-id="483bd-229">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="483bd-229">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="483bd-230">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="483bd-230">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="483bd-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="483bd-231">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="483bd-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="483bd-232">Search-Flags</span></span>           | <span data-ttu-id="483bd-233">0x00000001</span><span class="sxs-lookup"><span data-stu-id="483bd-233">0x00000001</span></span>                                                   |
| <span data-ttu-id="483bd-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="483bd-234">System-Flags</span></span>           | <span data-ttu-id="483bd-235">0x00000012</span><span class="sxs-lookup"><span data-stu-id="483bd-235">0x00000012</span></span>                                                   |
| <span data-ttu-id="483bd-236">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="483bd-236">Classes used in</span></span>        | [<span data-ttu-id="483bd-237">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="483bd-237">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="483bd-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="483bd-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="483bd-239">Eingabe</span><span class="sxs-lookup"><span data-stu-id="483bd-239">Entry</span></span> | <span data-ttu-id="483bd-240">Wert</span><span class="sxs-lookup"><span data-stu-id="483bd-240">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="483bd-241">Link-ID</span><span class="sxs-lookup"><span data-stu-id="483bd-241">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="483bd-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="483bd-242">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="483bd-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="483bd-243">System-Only</span></span>            | <span data-ttu-id="483bd-244">False</span><span class="sxs-lookup"><span data-stu-id="483bd-244">False</span></span>                                                        |
| <span data-ttu-id="483bd-245">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="483bd-245">Is-Single-Valued</span></span>       | <span data-ttu-id="483bd-246">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-246">True</span></span>                                                         |
| <span data-ttu-id="483bd-247">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="483bd-247">Is Indexed</span></span>             | <span data-ttu-id="483bd-248">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-248">True</span></span>                                                         |
| <span data-ttu-id="483bd-249">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="483bd-249">In Global Catalog</span></span>      | <span data-ttu-id="483bd-250">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-250">True</span></span>                                                         |
| <span data-ttu-id="483bd-251">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="483bd-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="483bd-252">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="483bd-252">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="483bd-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="483bd-253">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="483bd-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="483bd-254">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="483bd-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="483bd-255">Search-Flags</span></span>           | <span data-ttu-id="483bd-256">0x00000001</span><span class="sxs-lookup"><span data-stu-id="483bd-256">0x00000001</span></span>                                                   |
| <span data-ttu-id="483bd-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="483bd-257">System-Flags</span></span>           | <span data-ttu-id="483bd-258">0x00000012</span><span class="sxs-lookup"><span data-stu-id="483bd-258">0x00000012</span></span>                                                   |
| <span data-ttu-id="483bd-259">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="483bd-259">Classes used in</span></span>        | [<span data-ttu-id="483bd-260">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="483bd-260">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="483bd-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="483bd-261">Windows Server 2012</span></span>



| <span data-ttu-id="483bd-262">Eingabe</span><span class="sxs-lookup"><span data-stu-id="483bd-262">Entry</span></span> | <span data-ttu-id="483bd-263">Wert</span><span class="sxs-lookup"><span data-stu-id="483bd-263">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="483bd-264">Link-ID</span><span class="sxs-lookup"><span data-stu-id="483bd-264">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="483bd-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="483bd-265">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="483bd-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="483bd-266">System-Only</span></span>            | <span data-ttu-id="483bd-267">False</span><span class="sxs-lookup"><span data-stu-id="483bd-267">False</span></span>                                                        |
| <span data-ttu-id="483bd-268">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="483bd-268">Is-Single-Valued</span></span>       | <span data-ttu-id="483bd-269">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-269">True</span></span>                                                         |
| <span data-ttu-id="483bd-270">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="483bd-270">Is Indexed</span></span>             | <span data-ttu-id="483bd-271">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-271">True</span></span>                                                         |
| <span data-ttu-id="483bd-272">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="483bd-272">In Global Catalog</span></span>      | <span data-ttu-id="483bd-273">Richtig</span><span class="sxs-lookup"><span data-stu-id="483bd-273">True</span></span>                                                         |
| <span data-ttu-id="483bd-274">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="483bd-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="483bd-275">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="483bd-275">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="483bd-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="483bd-276">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="483bd-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="483bd-277">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="483bd-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="483bd-278">Search-Flags</span></span>           | <span data-ttu-id="483bd-279">0x00000001</span><span class="sxs-lookup"><span data-stu-id="483bd-279">0x00000001</span></span>                                                   |
| <span data-ttu-id="483bd-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="483bd-280">System-Flags</span></span>           | <span data-ttu-id="483bd-281">0x00000012</span><span class="sxs-lookup"><span data-stu-id="483bd-281">0x00000012</span></span>                                                   |
| <span data-ttu-id="483bd-282">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="483bd-282">Classes used in</span></span>        | [<span data-ttu-id="483bd-283">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="483bd-283">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





