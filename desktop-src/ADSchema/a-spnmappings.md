---
title: SPN-Mappings-Attribut
description: Dieses Attribut mit mehreren Werten enthält eine Liste von Dienst Prinzipal Namen (SPN), um die Äquivalenz von SPN-Typen anzuzeigen.
ms.assetid: 6d37618d-426d-4e7b-8475-c912adb595ee
ms.tgt_platform: multiple
keywords:
- AD-Schema für SPN-Mappings-Attribut
- spnmappings-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- SPN-Mappings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ccb07e068a22d0a85928832890f0b66ebda016
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519983"
---
# <a name="spn-mappings-attribute"></a><span data-ttu-id="42e6a-105">SPN-Mappings-Attribut</span><span class="sxs-lookup"><span data-stu-id="42e6a-105">SPN-Mappings attribute</span></span>

<span data-ttu-id="42e6a-106">Dieses Attribut mit mehreren Werten enthält eine Liste von Dienst Prinzipal Namen (SPN), um die Äquivalenz von SPN-Typen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="42e6a-106">This multiple-valued attribute contains a list of service principal names (SPN) to show the equivalence of SPN types.</span></span> <span data-ttu-id="42e6a-107">Der SPN ist der Name, den ein Client zum eindeutigen Identifizieren einer Instanz eines Dienstanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="42e6a-107">The SPN is the name a client uses to uniquely identify an instance of a service.</span></span> <span data-ttu-id="42e6a-108">Wenn Sie mehrere Instanzen eines Diensts auf Computern innerhalb einer Gesamtstruktur installieren, muss jede Instanz über einen eigenen SPN verfügen.</span><span class="sxs-lookup"><span data-stu-id="42e6a-108">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="42e6a-109">Eine Dienstinstanz kann mehrere SPNs aufweisen, falls mehrere Namen vorhanden sind, die von den Clients zur Authentifizierung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="42e6a-109">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span> <span data-ttu-id="42e6a-110">Beispiel: "LDAP/..." SPNs können zugeordnet werden, damit Sie "Host/..." entsprechen. SPNs.</span><span class="sxs-lookup"><span data-stu-id="42e6a-110">For example, "ldap/..." SPNs could be mapped so that they are equivalent to "host/..." SPNs.</span></span>



| <span data-ttu-id="42e6a-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="42e6a-111">Entry</span></span> | <span data-ttu-id="42e6a-112">Wert</span><span class="sxs-lookup"><span data-stu-id="42e6a-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42e6a-113">CN</span><span class="sxs-lookup"><span data-stu-id="42e6a-113">CN</span></span>                | <span data-ttu-id="42e6a-114">SPN-Mappings</span><span class="sxs-lookup"><span data-stu-id="42e6a-114">SPN-Mappings</span></span>                                                                                                       |
| <span data-ttu-id="42e6a-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="42e6a-115">Ldap-Display-Name</span></span> | <span data-ttu-id="42e6a-116">spnmappings</span><span class="sxs-lookup"><span data-stu-id="42e6a-116">sPNMappings</span></span>                                                                                                        |
| <span data-ttu-id="42e6a-117">Size</span><span class="sxs-lookup"><span data-stu-id="42e6a-117">Size</span></span>              | \-                                                                                                                 |
| <span data-ttu-id="42e6a-118">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="42e6a-118">Update Privilege</span></span>  | <span data-ttu-id="42e6a-119">Dieser Wert wird während der Produktinstallation festgelegt.</span><span class="sxs-lookup"><span data-stu-id="42e6a-119">This value is set during the product installation.</span></span> <span data-ttu-id="42e6a-120">Diese kann vom Systemadministrator zu einem späteren Zeitpunkt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="42e6a-120">It can be modified by the system administrator at a later time.</span></span> |
| <span data-ttu-id="42e6a-121">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="42e6a-121">Update Frequency</span></span>  | \-                                                                                                                 |
| <span data-ttu-id="42e6a-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="42e6a-122">Attribute-Id</span></span>      | <span data-ttu-id="42e6a-123">1.2.840.113556.1.4.1347</span><span class="sxs-lookup"><span data-stu-id="42e6a-123">1.2.840.113556.1.4.1347</span></span>                                                                                            |
| <span data-ttu-id="42e6a-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="42e6a-124">System-Id-Guid</span></span>    | <span data-ttu-id="42e6a-125">2ab0e76c-7041-11d2-9905-0000f 87a57d4</span><span class="sxs-lookup"><span data-stu-id="42e6a-125">2ab0e76c-7041-11d2-9905-0000f87a57d4</span></span>                                                                               |
| <span data-ttu-id="42e6a-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="42e6a-126">Syntax</span></span>            | [<span data-ttu-id="42e6a-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="42e6a-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                        |



## <a name="implementations"></a><span data-ttu-id="42e6a-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="42e6a-128">Implementations</span></span>

-   [<span data-ttu-id="42e6a-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="42e6a-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="42e6a-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="42e6a-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="42e6a-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="42e6a-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="42e6a-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="42e6a-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="42e6a-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="42e6a-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="42e6a-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="42e6a-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="42e6a-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="42e6a-135">Windows 2000 Server</span></span>



| <span data-ttu-id="42e6a-136">Eingabe</span><span class="sxs-lookup"><span data-stu-id="42e6a-136">Entry</span></span> | <span data-ttu-id="42e6a-137">Wert</span><span class="sxs-lookup"><span data-stu-id="42e6a-137">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="42e6a-138">Link-ID</span><span class="sxs-lookup"><span data-stu-id="42e6a-138">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="42e6a-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42e6a-139">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="42e6a-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="42e6a-140">System-Only</span></span>            | <span data-ttu-id="42e6a-141">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-141">False</span></span>                                            |
| <span data-ttu-id="42e6a-142">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="42e6a-142">Is-Single-Valued</span></span>       | <span data-ttu-id="42e6a-143">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-143">False</span></span>                                            |
| <span data-ttu-id="42e6a-144">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="42e6a-144">Is Indexed</span></span>             | <span data-ttu-id="42e6a-145">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-145">False</span></span>                                            |
| <span data-ttu-id="42e6a-146">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="42e6a-146">In Global Catalog</span></span>      | <span data-ttu-id="42e6a-147">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-147">False</span></span>                                            |
| <span data-ttu-id="42e6a-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42e6a-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="42e6a-149">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="42e6a-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="42e6a-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42e6a-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="42e6a-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42e6a-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="42e6a-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42e6a-152">Search-Flags</span></span>           | <span data-ttu-id="42e6a-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42e6a-153">0x00000000</span></span>                                       |
| <span data-ttu-id="42e6a-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42e6a-154">System-Flags</span></span>           | <span data-ttu-id="42e6a-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42e6a-155">0x00000010</span></span>                                       |
| <span data-ttu-id="42e6a-156">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="42e6a-156">Classes used in</span></span>        | [<span data-ttu-id="42e6a-157">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="42e6a-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="42e6a-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="42e6a-158">Windows Server 2003</span></span>



| <span data-ttu-id="42e6a-159">Eingabe</span><span class="sxs-lookup"><span data-stu-id="42e6a-159">Entry</span></span> | <span data-ttu-id="42e6a-160">Wert</span><span class="sxs-lookup"><span data-stu-id="42e6a-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="42e6a-161">Link-ID</span><span class="sxs-lookup"><span data-stu-id="42e6a-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="42e6a-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42e6a-162">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="42e6a-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="42e6a-163">System-Only</span></span>            | <span data-ttu-id="42e6a-164">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-164">False</span></span>                                            |
| <span data-ttu-id="42e6a-165">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="42e6a-165">Is-Single-Valued</span></span>       | <span data-ttu-id="42e6a-166">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-166">False</span></span>                                            |
| <span data-ttu-id="42e6a-167">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="42e6a-167">Is Indexed</span></span>             | <span data-ttu-id="42e6a-168">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-168">False</span></span>                                            |
| <span data-ttu-id="42e6a-169">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="42e6a-169">In Global Catalog</span></span>      | <span data-ttu-id="42e6a-170">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-170">False</span></span>                                            |
| <span data-ttu-id="42e6a-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42e6a-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="42e6a-172">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="42e6a-172">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="42e6a-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42e6a-173">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="42e6a-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42e6a-174">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="42e6a-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42e6a-175">Search-Flags</span></span>           | <span data-ttu-id="42e6a-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42e6a-176">0x00000000</span></span>                                       |
| <span data-ttu-id="42e6a-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42e6a-177">System-Flags</span></span>           | <span data-ttu-id="42e6a-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42e6a-178">0x00000010</span></span>                                       |
| <span data-ttu-id="42e6a-179">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="42e6a-179">Classes used in</span></span>        | [<span data-ttu-id="42e6a-180">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="42e6a-180">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="42e6a-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="42e6a-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="42e6a-182">Eingabe</span><span class="sxs-lookup"><span data-stu-id="42e6a-182">Entry</span></span> | <span data-ttu-id="42e6a-183">Wert</span><span class="sxs-lookup"><span data-stu-id="42e6a-183">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="42e6a-184">Link-ID</span><span class="sxs-lookup"><span data-stu-id="42e6a-184">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="42e6a-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42e6a-185">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="42e6a-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="42e6a-186">System-Only</span></span>            | <span data-ttu-id="42e6a-187">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-187">False</span></span>                                            |
| <span data-ttu-id="42e6a-188">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="42e6a-188">Is-Single-Valued</span></span>       | <span data-ttu-id="42e6a-189">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-189">False</span></span>                                            |
| <span data-ttu-id="42e6a-190">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="42e6a-190">Is Indexed</span></span>             | <span data-ttu-id="42e6a-191">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-191">False</span></span>                                            |
| <span data-ttu-id="42e6a-192">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="42e6a-192">In Global Catalog</span></span>      | <span data-ttu-id="42e6a-193">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-193">False</span></span>                                            |
| <span data-ttu-id="42e6a-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42e6a-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="42e6a-195">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="42e6a-195">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="42e6a-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42e6a-196">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="42e6a-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42e6a-197">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="42e6a-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42e6a-198">Search-Flags</span></span>           | <span data-ttu-id="42e6a-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42e6a-199">0x00000000</span></span>                                       |
| <span data-ttu-id="42e6a-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42e6a-200">System-Flags</span></span>           | <span data-ttu-id="42e6a-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42e6a-201">0x00000010</span></span>                                       |
| <span data-ttu-id="42e6a-202">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="42e6a-202">Classes used in</span></span>        | [<span data-ttu-id="42e6a-203">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="42e6a-203">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="42e6a-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42e6a-204">Windows Server 2008</span></span>



| <span data-ttu-id="42e6a-205">Eingabe</span><span class="sxs-lookup"><span data-stu-id="42e6a-205">Entry</span></span> | <span data-ttu-id="42e6a-206">Wert</span><span class="sxs-lookup"><span data-stu-id="42e6a-206">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="42e6a-207">Link-ID</span><span class="sxs-lookup"><span data-stu-id="42e6a-207">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="42e6a-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42e6a-208">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="42e6a-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="42e6a-209">System-Only</span></span>            | <span data-ttu-id="42e6a-210">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-210">False</span></span>                                            |
| <span data-ttu-id="42e6a-211">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="42e6a-211">Is-Single-Valued</span></span>       | <span data-ttu-id="42e6a-212">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-212">False</span></span>                                            |
| <span data-ttu-id="42e6a-213">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="42e6a-213">Is Indexed</span></span>             | <span data-ttu-id="42e6a-214">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-214">False</span></span>                                            |
| <span data-ttu-id="42e6a-215">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="42e6a-215">In Global Catalog</span></span>      | <span data-ttu-id="42e6a-216">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-216">False</span></span>                                            |
| <span data-ttu-id="42e6a-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42e6a-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="42e6a-218">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="42e6a-218">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="42e6a-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42e6a-219">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="42e6a-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42e6a-220">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="42e6a-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42e6a-221">Search-Flags</span></span>           | <span data-ttu-id="42e6a-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42e6a-222">0x00000000</span></span>                                       |
| <span data-ttu-id="42e6a-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42e6a-223">System-Flags</span></span>           | <span data-ttu-id="42e6a-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42e6a-224">0x00000010</span></span>                                       |
| <span data-ttu-id="42e6a-225">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="42e6a-225">Classes used in</span></span>        | [<span data-ttu-id="42e6a-226">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="42e6a-226">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="42e6a-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="42e6a-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="42e6a-228">Eingabe</span><span class="sxs-lookup"><span data-stu-id="42e6a-228">Entry</span></span> | <span data-ttu-id="42e6a-229">Wert</span><span class="sxs-lookup"><span data-stu-id="42e6a-229">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="42e6a-230">Link-ID</span><span class="sxs-lookup"><span data-stu-id="42e6a-230">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="42e6a-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42e6a-231">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="42e6a-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="42e6a-232">System-Only</span></span>            | <span data-ttu-id="42e6a-233">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-233">False</span></span>                                            |
| <span data-ttu-id="42e6a-234">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="42e6a-234">Is-Single-Valued</span></span>       | <span data-ttu-id="42e6a-235">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-235">False</span></span>                                            |
| <span data-ttu-id="42e6a-236">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="42e6a-236">Is Indexed</span></span>             | <span data-ttu-id="42e6a-237">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-237">False</span></span>                                            |
| <span data-ttu-id="42e6a-238">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="42e6a-238">In Global Catalog</span></span>      | <span data-ttu-id="42e6a-239">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-239">False</span></span>                                            |
| <span data-ttu-id="42e6a-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42e6a-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="42e6a-241">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="42e6a-241">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="42e6a-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42e6a-242">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="42e6a-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42e6a-243">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="42e6a-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42e6a-244">Search-Flags</span></span>           | <span data-ttu-id="42e6a-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42e6a-245">0x00000000</span></span>                                       |
| <span data-ttu-id="42e6a-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42e6a-246">System-Flags</span></span>           | <span data-ttu-id="42e6a-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42e6a-247">0x00000010</span></span>                                       |
| <span data-ttu-id="42e6a-248">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="42e6a-248">Classes used in</span></span>        | [<span data-ttu-id="42e6a-249">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="42e6a-249">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="42e6a-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="42e6a-250">Windows Server 2012</span></span>



| <span data-ttu-id="42e6a-251">Eingabe</span><span class="sxs-lookup"><span data-stu-id="42e6a-251">Entry</span></span> | <span data-ttu-id="42e6a-252">Wert</span><span class="sxs-lookup"><span data-stu-id="42e6a-252">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="42e6a-253">Link-ID</span><span class="sxs-lookup"><span data-stu-id="42e6a-253">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="42e6a-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42e6a-254">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="42e6a-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="42e6a-255">System-Only</span></span>            | <span data-ttu-id="42e6a-256">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-256">False</span></span>                                            |
| <span data-ttu-id="42e6a-257">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="42e6a-257">Is-Single-Valued</span></span>       | <span data-ttu-id="42e6a-258">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-258">False</span></span>                                            |
| <span data-ttu-id="42e6a-259">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="42e6a-259">Is Indexed</span></span>             | <span data-ttu-id="42e6a-260">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-260">False</span></span>                                            |
| <span data-ttu-id="42e6a-261">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="42e6a-261">In Global Catalog</span></span>      | <span data-ttu-id="42e6a-262">False</span><span class="sxs-lookup"><span data-stu-id="42e6a-262">False</span></span>                                            |
| <span data-ttu-id="42e6a-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="42e6a-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="42e6a-264">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="42e6a-264">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="42e6a-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42e6a-265">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="42e6a-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42e6a-266">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="42e6a-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42e6a-267">Search-Flags</span></span>           | <span data-ttu-id="42e6a-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42e6a-268">0x00000000</span></span>                                       |
| <span data-ttu-id="42e6a-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42e6a-269">System-Flags</span></span>           | <span data-ttu-id="42e6a-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42e6a-270">0x00000010</span></span>                                       |
| <span data-ttu-id="42e6a-271">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="42e6a-271">Classes used in</span></span>        | [<span data-ttu-id="42e6a-272">**NTDS-Dienst**</span><span class="sxs-lookup"><span data-stu-id="42e6a-272">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





