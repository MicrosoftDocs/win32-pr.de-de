---
title: Sam-Account-Name-Attribut
description: Der Anmelde Name, der zur Unterstützung von Clients und Servern verwendet wird, auf denen frühere Versionen des Betriebssystems ausgeführt werden, z. b. Windows NT 4,0, Windows 95, Windows 98 und LAN-Manager.
ms.assetid: dc661e59-9a36-4d2b-93f0-f88edf7efd66
ms.tgt_platform: multiple
keywords:
- "\"Sam-Account-Name\"-Attribut AD-Schema"
- sAMAccountName-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- SAM-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb64cba7825c3b4400641cdc5c62890f64bc299
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859764"
---
# <a name="sam-account-name-attribute"></a><span data-ttu-id="5a97e-105">Sam-Account-Name-Attribut</span><span class="sxs-lookup"><span data-stu-id="5a97e-105">SAM-Account-Name attribute</span></span>

<span data-ttu-id="5a97e-106">Der Anmelde Name, der zur Unterstützung von Clients und Servern verwendet wird, auf denen frühere Versionen des Betriebssystems ausgeführt werden, z. b. Windows NT 4,0, Windows 95, Windows 98 und LAN-Manager.</span><span class="sxs-lookup"><span data-stu-id="5a97e-106">The logon name used to support clients and servers running earlier versions of the operating system, such as Windows NT 4.0, Windows 95, Windows 98, and LAN Manager.</span></span>

<span data-ttu-id="5a97e-107">Dieses Attribut darf maximal 20 Zeichen lang sein, um frühere Clients zu unterstützen, und darf keines der folgenden Zeichen enthalten:</span><span class="sxs-lookup"><span data-stu-id="5a97e-107">This attribute must be 20 characters or less to support earlier clients, and cannot contain any of these characters:</span></span>

-   <span data-ttu-id="5a97e-108">"/ \\ \[ \] : ; \| = , + \* ?</span><span class="sxs-lookup"><span data-stu-id="5a97e-108">"/ \\ \[ \] : ; \| = , + \* ?</span></span> <span data-ttu-id="5a97e-109">< ></span><span class="sxs-lookup"><span data-stu-id="5a97e-109">< ></span></span>



| <span data-ttu-id="5a97e-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a97e-110">Entry</span></span> | <span data-ttu-id="5a97e-111">Wert</span><span class="sxs-lookup"><span data-stu-id="5a97e-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a97e-112">CN</span><span class="sxs-lookup"><span data-stu-id="5a97e-112">CN</span></span>                | <span data-ttu-id="5a97e-113">Sam-Account-Name</span><span class="sxs-lookup"><span data-stu-id="5a97e-113">SAM-Account-Name</span></span>                                                                         |
| <span data-ttu-id="5a97e-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5a97e-114">Ldap-Display-Name</span></span> | <span data-ttu-id="5a97e-115">sAMAccountName</span><span class="sxs-lookup"><span data-stu-id="5a97e-115">sAMAccountName</span></span>                                                                           |
| <span data-ttu-id="5a97e-116">Size</span><span class="sxs-lookup"><span data-stu-id="5a97e-116">Size</span></span>              | <span data-ttu-id="5a97e-117">maximal 20 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="5a97e-117">20 characters or less.</span></span>                                                                   |
| <span data-ttu-id="5a97e-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5a97e-118">Update Privilege</span></span>  | <span data-ttu-id="5a97e-119">Domänen Administrator</span><span class="sxs-lookup"><span data-stu-id="5a97e-119">Domain administrator</span></span>                                                                     |
| <span data-ttu-id="5a97e-120">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="5a97e-120">Update Frequency</span></span>  | <span data-ttu-id="5a97e-121">Dieser Wert sollte beim Erstellen des Kontodaten Satzes zugewiesen werden und sollte nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5a97e-121">This value should be assigned when the account record is created, and should not change.</span></span> |
| <span data-ttu-id="5a97e-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5a97e-122">Attribute-Id</span></span>      | <span data-ttu-id="5a97e-123">1.2.840.113556.1.4.221</span><span class="sxs-lookup"><span data-stu-id="5a97e-123">1.2.840.113556.1.4.221</span></span>                                                                   |
| <span data-ttu-id="5a97e-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5a97e-124">System-Id-Guid</span></span>    | <span data-ttu-id="5a97e-125">3e0abf D0-126a-11D0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="5a97e-125">3e0abfd0-126a-11d0-a060-00aa006c33ed</span></span>                                                     |
| <span data-ttu-id="5a97e-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a97e-126">Syntax</span></span>            | [<span data-ttu-id="5a97e-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5a97e-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                              |



## <a name="implementations"></a><span data-ttu-id="5a97e-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="5a97e-128">Implementations</span></span>

-   [<span data-ttu-id="5a97e-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5a97e-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5a97e-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5a97e-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5a97e-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5a97e-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5a97e-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5a97e-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5a97e-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5a97e-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5a97e-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5a97e-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5a97e-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5a97e-135">Windows 2000 Server</span></span>



| <span data-ttu-id="5a97e-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a97e-136">Entry</span></span> | <span data-ttu-id="5a97e-137">Wert</span><span class="sxs-lookup"><span data-stu-id="5a97e-137">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5a97e-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a97e-138">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5a97e-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a97e-139">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5a97e-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a97e-140">System-Only</span></span>            | <span data-ttu-id="5a97e-141">False</span><span class="sxs-lookup"><span data-stu-id="5a97e-141">False</span></span>                                                        |
| <span data-ttu-id="5a97e-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a97e-142">Is-Single-Valued</span></span>       | <span data-ttu-id="5a97e-143">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-143">True</span></span>                                                         |
| <span data-ttu-id="5a97e-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a97e-144">Is Indexed</span></span>             | <span data-ttu-id="5a97e-145">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-145">True</span></span>                                                         |
| <span data-ttu-id="5a97e-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a97e-146">In Global Catalog</span></span>      | <span data-ttu-id="5a97e-147">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-147">True</span></span>                                                         |
| <span data-ttu-id="5a97e-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a97e-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a97e-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a97e-149">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5a97e-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a97e-150">Range-Lower</span></span>            | <span data-ttu-id="5a97e-151">0</span><span class="sxs-lookup"><span data-stu-id="5a97e-151">0</span></span>                                                            |
| <span data-ttu-id="5a97e-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a97e-152">Range-Upper</span></span>            | <span data-ttu-id="5a97e-153">256</span><span class="sxs-lookup"><span data-stu-id="5a97e-153">256</span></span>                                                          |
| <span data-ttu-id="5a97e-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a97e-154">Search-Flags</span></span>           | <span data-ttu-id="5a97e-155">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="5a97e-155">0x0000000D</span></span>                                                   |
| <span data-ttu-id="5a97e-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a97e-156">System-Flags</span></span>           | <span data-ttu-id="5a97e-157">0x00000012</span><span class="sxs-lookup"><span data-stu-id="5a97e-157">0x00000012</span></span>                                                   |
| <span data-ttu-id="5a97e-158">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a97e-158">Classes used in</span></span>        | [<span data-ttu-id="5a97e-159">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="5a97e-159">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5a97e-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5a97e-160">Windows Server 2003</span></span>



| <span data-ttu-id="5a97e-161">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a97e-161">Entry</span></span> | <span data-ttu-id="5a97e-162">Wert</span><span class="sxs-lookup"><span data-stu-id="5a97e-162">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5a97e-163">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a97e-163">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5a97e-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a97e-164">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5a97e-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a97e-165">System-Only</span></span>            | <span data-ttu-id="5a97e-166">False</span><span class="sxs-lookup"><span data-stu-id="5a97e-166">False</span></span>                                                        |
| <span data-ttu-id="5a97e-167">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a97e-167">Is-Single-Valued</span></span>       | <span data-ttu-id="5a97e-168">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-168">True</span></span>                                                         |
| <span data-ttu-id="5a97e-169">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a97e-169">Is Indexed</span></span>             | <span data-ttu-id="5a97e-170">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-170">True</span></span>                                                         |
| <span data-ttu-id="5a97e-171">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a97e-171">In Global Catalog</span></span>      | <span data-ttu-id="5a97e-172">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-172">True</span></span>                                                         |
| <span data-ttu-id="5a97e-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a97e-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a97e-174">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a97e-174">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5a97e-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a97e-175">Range-Lower</span></span>            | <span data-ttu-id="5a97e-176">0</span><span class="sxs-lookup"><span data-stu-id="5a97e-176">0</span></span>                                                            |
| <span data-ttu-id="5a97e-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a97e-177">Range-Upper</span></span>            | <span data-ttu-id="5a97e-178">256</span><span class="sxs-lookup"><span data-stu-id="5a97e-178">256</span></span>                                                          |
| <span data-ttu-id="5a97e-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a97e-179">Search-Flags</span></span>           | <span data-ttu-id="5a97e-180">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="5a97e-180">0x0000000D</span></span>                                                   |
| <span data-ttu-id="5a97e-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a97e-181">System-Flags</span></span>           | <span data-ttu-id="5a97e-182">0x00000012</span><span class="sxs-lookup"><span data-stu-id="5a97e-182">0x00000012</span></span>                                                   |
| <span data-ttu-id="5a97e-183">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a97e-183">Classes used in</span></span>        | [<span data-ttu-id="5a97e-184">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="5a97e-184">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5a97e-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5a97e-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5a97e-186">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a97e-186">Entry</span></span> | <span data-ttu-id="5a97e-187">Wert</span><span class="sxs-lookup"><span data-stu-id="5a97e-187">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5a97e-188">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a97e-188">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5a97e-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a97e-189">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5a97e-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a97e-190">System-Only</span></span>            | <span data-ttu-id="5a97e-191">False</span><span class="sxs-lookup"><span data-stu-id="5a97e-191">False</span></span>                                                        |
| <span data-ttu-id="5a97e-192">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a97e-192">Is-Single-Valued</span></span>       | <span data-ttu-id="5a97e-193">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-193">True</span></span>                                                         |
| <span data-ttu-id="5a97e-194">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a97e-194">Is Indexed</span></span>             | <span data-ttu-id="5a97e-195">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-195">True</span></span>                                                         |
| <span data-ttu-id="5a97e-196">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a97e-196">In Global Catalog</span></span>      | <span data-ttu-id="5a97e-197">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-197">True</span></span>                                                         |
| <span data-ttu-id="5a97e-198">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a97e-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a97e-199">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a97e-199">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5a97e-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a97e-200">Range-Lower</span></span>            | <span data-ttu-id="5a97e-201">0</span><span class="sxs-lookup"><span data-stu-id="5a97e-201">0</span></span>                                                            |
| <span data-ttu-id="5a97e-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a97e-202">Range-Upper</span></span>            | <span data-ttu-id="5a97e-203">256</span><span class="sxs-lookup"><span data-stu-id="5a97e-203">256</span></span>                                                          |
| <span data-ttu-id="5a97e-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a97e-204">Search-Flags</span></span>           | <span data-ttu-id="5a97e-205">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="5a97e-205">0x0000000D</span></span>                                                   |
| <span data-ttu-id="5a97e-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a97e-206">System-Flags</span></span>           | <span data-ttu-id="5a97e-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="5a97e-207">0x00000012</span></span>                                                   |
| <span data-ttu-id="5a97e-208">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a97e-208">Classes used in</span></span>        | [<span data-ttu-id="5a97e-209">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="5a97e-209">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5a97e-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a97e-210">Windows Server 2008</span></span>



| <span data-ttu-id="5a97e-211">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a97e-211">Entry</span></span> | <span data-ttu-id="5a97e-212">Wert</span><span class="sxs-lookup"><span data-stu-id="5a97e-212">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5a97e-213">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a97e-213">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5a97e-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a97e-214">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5a97e-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a97e-215">System-Only</span></span>            | <span data-ttu-id="5a97e-216">False</span><span class="sxs-lookup"><span data-stu-id="5a97e-216">False</span></span>                                                        |
| <span data-ttu-id="5a97e-217">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a97e-217">Is-Single-Valued</span></span>       | <span data-ttu-id="5a97e-218">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-218">True</span></span>                                                         |
| <span data-ttu-id="5a97e-219">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a97e-219">Is Indexed</span></span>             | <span data-ttu-id="5a97e-220">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-220">True</span></span>                                                         |
| <span data-ttu-id="5a97e-221">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a97e-221">In Global Catalog</span></span>      | <span data-ttu-id="5a97e-222">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-222">True</span></span>                                                         |
| <span data-ttu-id="5a97e-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a97e-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a97e-224">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a97e-224">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5a97e-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a97e-225">Range-Lower</span></span>            | <span data-ttu-id="5a97e-226">0</span><span class="sxs-lookup"><span data-stu-id="5a97e-226">0</span></span>                                                            |
| <span data-ttu-id="5a97e-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a97e-227">Range-Upper</span></span>            | <span data-ttu-id="5a97e-228">256</span><span class="sxs-lookup"><span data-stu-id="5a97e-228">256</span></span>                                                          |
| <span data-ttu-id="5a97e-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a97e-229">Search-Flags</span></span>           | <span data-ttu-id="5a97e-230">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="5a97e-230">0x0000000D</span></span>                                                   |
| <span data-ttu-id="5a97e-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a97e-231">System-Flags</span></span>           | <span data-ttu-id="5a97e-232">0x00000012</span><span class="sxs-lookup"><span data-stu-id="5a97e-232">0x00000012</span></span>                                                   |
| <span data-ttu-id="5a97e-233">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a97e-233">Classes used in</span></span>        | [<span data-ttu-id="5a97e-234">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="5a97e-234">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5a97e-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5a97e-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5a97e-236">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a97e-236">Entry</span></span> | <span data-ttu-id="5a97e-237">Wert</span><span class="sxs-lookup"><span data-stu-id="5a97e-237">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5a97e-238">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a97e-238">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5a97e-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a97e-239">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5a97e-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a97e-240">System-Only</span></span>            | <span data-ttu-id="5a97e-241">False</span><span class="sxs-lookup"><span data-stu-id="5a97e-241">False</span></span>                                                        |
| <span data-ttu-id="5a97e-242">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a97e-242">Is-Single-Valued</span></span>       | <span data-ttu-id="5a97e-243">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-243">True</span></span>                                                         |
| <span data-ttu-id="5a97e-244">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a97e-244">Is Indexed</span></span>             | <span data-ttu-id="5a97e-245">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-245">True</span></span>                                                         |
| <span data-ttu-id="5a97e-246">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a97e-246">In Global Catalog</span></span>      | <span data-ttu-id="5a97e-247">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-247">True</span></span>                                                         |
| <span data-ttu-id="5a97e-248">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a97e-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a97e-249">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a97e-249">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5a97e-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a97e-250">Range-Lower</span></span>            | <span data-ttu-id="5a97e-251">0</span><span class="sxs-lookup"><span data-stu-id="5a97e-251">0</span></span>                                                            |
| <span data-ttu-id="5a97e-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a97e-252">Range-Upper</span></span>            | <span data-ttu-id="5a97e-253">256</span><span class="sxs-lookup"><span data-stu-id="5a97e-253">256</span></span>                                                          |
| <span data-ttu-id="5a97e-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a97e-254">Search-Flags</span></span>           | <span data-ttu-id="5a97e-255">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="5a97e-255">0x0000000D</span></span>                                                   |
| <span data-ttu-id="5a97e-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a97e-256">System-Flags</span></span>           | <span data-ttu-id="5a97e-257">0x00000012</span><span class="sxs-lookup"><span data-stu-id="5a97e-257">0x00000012</span></span>                                                   |
| <span data-ttu-id="5a97e-258">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a97e-258">Classes used in</span></span>        | [<span data-ttu-id="5a97e-259">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="5a97e-259">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5a97e-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5a97e-260">Windows Server 2012</span></span>



| <span data-ttu-id="5a97e-261">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a97e-261">Entry</span></span> | <span data-ttu-id="5a97e-262">Wert</span><span class="sxs-lookup"><span data-stu-id="5a97e-262">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5a97e-263">Link-ID</span><span class="sxs-lookup"><span data-stu-id="5a97e-263">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5a97e-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a97e-264">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5a97e-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a97e-265">System-Only</span></span>            | <span data-ttu-id="5a97e-266">False</span><span class="sxs-lookup"><span data-stu-id="5a97e-266">False</span></span>                                                        |
| <span data-ttu-id="5a97e-267">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="5a97e-267">Is-Single-Valued</span></span>       | <span data-ttu-id="5a97e-268">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-268">True</span></span>                                                         |
| <span data-ttu-id="5a97e-269">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="5a97e-269">Is Indexed</span></span>             | <span data-ttu-id="5a97e-270">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-270">True</span></span>                                                         |
| <span data-ttu-id="5a97e-271">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="5a97e-271">In Global Catalog</span></span>      | <span data-ttu-id="5a97e-272">Richtig</span><span class="sxs-lookup"><span data-stu-id="5a97e-272">True</span></span>                                                         |
| <span data-ttu-id="5a97e-273">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5a97e-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a97e-274">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="5a97e-274">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5a97e-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a97e-275">Range-Lower</span></span>            | <span data-ttu-id="5a97e-276">0</span><span class="sxs-lookup"><span data-stu-id="5a97e-276">0</span></span>                                                            |
| <span data-ttu-id="5a97e-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a97e-277">Range-Upper</span></span>            | <span data-ttu-id="5a97e-278">256</span><span class="sxs-lookup"><span data-stu-id="5a97e-278">256</span></span>                                                          |
| <span data-ttu-id="5a97e-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a97e-279">Search-Flags</span></span>           | <span data-ttu-id="5a97e-280">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="5a97e-280">0x0000000D</span></span>                                                   |
| <span data-ttu-id="5a97e-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a97e-281">System-Flags</span></span>           | <span data-ttu-id="5a97e-282">0x00000012</span><span class="sxs-lookup"><span data-stu-id="5a97e-282">0x00000012</span></span>                                                   |
| <span data-ttu-id="5a97e-283">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="5a97e-283">Classes used in</span></span>        | [<span data-ttu-id="5a97e-284">**Sicherheits Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="5a97e-284">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





