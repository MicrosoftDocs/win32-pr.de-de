---
title: Entry-TTL-Attribut
description: Dieses Betriebs Attribut wird vom Server verwaltet und ist anscheinend in jedem dynamischen Eintrag vorhanden.
ms.assetid: cac0e52e-243d-4822-9419-2af8b9352cee
ms.tgt_platform: multiple
keywords:
- AD-Schema für Entry-TTL-Attribut
- entryttl-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Entry-TTL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2dd5e38b22731fee7f957ee8f817537e32c645
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479711"
---
# <a name="entry-ttl-attribute"></a><span data-ttu-id="1efa2-105">Entry-TTL-Attribut</span><span class="sxs-lookup"><span data-stu-id="1efa2-105">Entry-TTL attribute</span></span>

<span data-ttu-id="1efa2-106">Dieses Betriebs Attribut wird vom Server verwaltet und ist anscheinend in jedem dynamischen Eintrag vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1efa2-106">This operational attribute is maintained by the server and appears to be present in every dynamic entry.</span></span> <span data-ttu-id="1efa2-107">Das-Attribut ist nicht vorhanden, wenn der Eintrag nicht die DynamicObject-Objektklasse enthält.</span><span class="sxs-lookup"><span data-stu-id="1efa2-107">The attribute is not present when the entry does not contain the dynamicObject object class.</span></span> <span data-ttu-id="1efa2-108">Der Wert dieses Attributs ist die Zeit (in Sekunden), in der der Eintrag weiterhin vorhanden ist, bevor er aus dem Verzeichnis verschwindet.</span><span class="sxs-lookup"><span data-stu-id="1efa2-108">The value of this attribute is the time, in seconds, that the entry will continue to exist before disappearing from the directory.</span></span> <span data-ttu-id="1efa2-109">Wenn keine dazwischenliegenden "Refresh"-Vorgänge vorhanden sind, werden die Werte, die durch das Lesen des Attributs in zwei aufeinander folgenden suchen zurückgegeben werden, garantiert nicht zunehmen.</span><span class="sxs-lookup"><span data-stu-id="1efa2-109">In the absence of intervening "refresh" operations, the values returned by reading the attribute in two successive searches are guaranteed to be nonincreasing.</span></span> <span data-ttu-id="1efa2-110">Der kleinste zulässige Wert ist 0 (null) und gibt an, dass der Eintrag ohne Warnung verschwinden kann.</span><span class="sxs-lookup"><span data-stu-id="1efa2-110">The smallest permissible value is 0, indicating that the entry may disappear without warning.</span></span> <span data-ttu-id="1efa2-111">Das Attribut ist als "keine Benutzer Änderung" gekennzeichnet, da es nur mit dem Aktualisierungs Vorgang geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1efa2-111">The attribute is marked NO-USER-MODIFICATION because it may only be changed by using the refresh operation.</span></span>



| <span data-ttu-id="1efa2-112">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1efa2-112">Entry</span></span> | <span data-ttu-id="1efa2-113">Wert</span><span class="sxs-lookup"><span data-stu-id="1efa2-113">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="1efa2-114">CN</span><span class="sxs-lookup"><span data-stu-id="1efa2-114">CN</span></span>                | <span data-ttu-id="1efa2-115">Entry-TTL</span><span class="sxs-lookup"><span data-stu-id="1efa2-115">Entry-TTL</span></span>                                   |
| <span data-ttu-id="1efa2-116">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1efa2-116">Ldap-Display-Name</span></span> | <span data-ttu-id="1efa2-117">entryttl</span><span class="sxs-lookup"><span data-stu-id="1efa2-117">entryTTL</span></span>                                    |
| <span data-ttu-id="1efa2-118">Size</span><span class="sxs-lookup"><span data-stu-id="1efa2-118">Size</span></span>              | <span data-ttu-id="1efa2-119">4 Bytes.</span><span class="sxs-lookup"><span data-stu-id="1efa2-119">4 bytes.</span></span> <span data-ttu-id="1efa2-120">Maximum = 1 Jahr, Standardwert = 1 Tag.</span><span class="sxs-lookup"><span data-stu-id="1efa2-120">Maximum = 1 year, default = 1 day.</span></span> |
| <span data-ttu-id="1efa2-121">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="1efa2-121">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="1efa2-122">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="1efa2-122">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="1efa2-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1efa2-123">Attribute-Id</span></span>      | <span data-ttu-id="1efa2-124">1.3.6.1.4.1.1466.101.119.3</span><span class="sxs-lookup"><span data-stu-id="1efa2-124">1.3.6.1.4.1.1466.101.119.3</span></span>                  |
| <span data-ttu-id="1efa2-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1efa2-125">System-Id-Guid</span></span>    | <span data-ttu-id="1efa2-126">d213decc-d81a-4384-aac2-dcfcfd631cf8</span><span class="sxs-lookup"><span data-stu-id="1efa2-126">d213decc-d81a-4384-aac2-dcfcfd631cf8</span></span>        |
| <span data-ttu-id="1efa2-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="1efa2-127">Syntax</span></span>            | [<span data-ttu-id="1efa2-128">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="1efa2-128">**Enumeration**</span></span>](s-enumeration.md)        |



## <a name="implementations"></a><span data-ttu-id="1efa2-129">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="1efa2-129">Implementations</span></span>

-   [<span data-ttu-id="1efa2-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1efa2-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1efa2-131">**Adam**</span><span class="sxs-lookup"><span data-stu-id="1efa2-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1efa2-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1efa2-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1efa2-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1efa2-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1efa2-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1efa2-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1efa2-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1efa2-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="1efa2-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1efa2-136">Windows Server 2003</span></span>



| <span data-ttu-id="1efa2-137">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1efa2-137">Entry</span></span> | <span data-ttu-id="1efa2-138">Wert</span><span class="sxs-lookup"><span data-stu-id="1efa2-138">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1efa2-139">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1efa2-139">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1efa2-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1efa2-140">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1efa2-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="1efa2-141">System-Only</span></span>            | <span data-ttu-id="1efa2-142">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-142">False</span></span>                                                |
| <span data-ttu-id="1efa2-143">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1efa2-143">Is-Single-Valued</span></span>       | <span data-ttu-id="1efa2-144">Richtig</span><span class="sxs-lookup"><span data-stu-id="1efa2-144">True</span></span>                                                 |
| <span data-ttu-id="1efa2-145">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1efa2-145">Is Indexed</span></span>             | <span data-ttu-id="1efa2-146">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-146">False</span></span>                                                |
| <span data-ttu-id="1efa2-147">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1efa2-147">In Global Catalog</span></span>      | <span data-ttu-id="1efa2-148">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-148">False</span></span>                                                |
| <span data-ttu-id="1efa2-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1efa2-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="1efa2-150">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1efa2-150">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1efa2-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1efa2-151">Range-Lower</span></span>            | <span data-ttu-id="1efa2-152">0</span><span class="sxs-lookup"><span data-stu-id="1efa2-152">0</span></span>                                                    |
| <span data-ttu-id="1efa2-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1efa2-153">Range-Upper</span></span>            | <span data-ttu-id="1efa2-154">31557600</span><span class="sxs-lookup"><span data-stu-id="1efa2-154">31557600</span></span>                                             |
| <span data-ttu-id="1efa2-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa2-155">Search-Flags</span></span>           | <span data-ttu-id="1efa2-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1efa2-156">0x00000000</span></span>                                           |
| <span data-ttu-id="1efa2-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa2-157">System-Flags</span></span>           | <span data-ttu-id="1efa2-158">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1efa2-158">0x00000014</span></span>                                           |
| <span data-ttu-id="1efa2-159">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1efa2-159">Classes used in</span></span>        | [<span data-ttu-id="1efa2-160">**Dynamic-Object**</span><span class="sxs-lookup"><span data-stu-id="1efa2-160">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1efa2-161">Adam</span><span class="sxs-lookup"><span data-stu-id="1efa2-161">ADAM</span></span>



| <span data-ttu-id="1efa2-162">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1efa2-162">Entry</span></span> | <span data-ttu-id="1efa2-163">Wert</span><span class="sxs-lookup"><span data-stu-id="1efa2-163">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1efa2-164">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1efa2-164">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1efa2-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1efa2-165">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1efa2-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="1efa2-166">System-Only</span></span>            | <span data-ttu-id="1efa2-167">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-167">False</span></span>                                                |
| <span data-ttu-id="1efa2-168">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1efa2-168">Is-Single-Valued</span></span>       | <span data-ttu-id="1efa2-169">Richtig</span><span class="sxs-lookup"><span data-stu-id="1efa2-169">True</span></span>                                                 |
| <span data-ttu-id="1efa2-170">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1efa2-170">Is Indexed</span></span>             | <span data-ttu-id="1efa2-171">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-171">False</span></span>                                                |
| <span data-ttu-id="1efa2-172">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1efa2-172">In Global Catalog</span></span>      | <span data-ttu-id="1efa2-173">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-173">False</span></span>                                                |
| <span data-ttu-id="1efa2-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1efa2-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="1efa2-175">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1efa2-175">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1efa2-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1efa2-176">Range-Lower</span></span>            | <span data-ttu-id="1efa2-177">0</span><span class="sxs-lookup"><span data-stu-id="1efa2-177">0</span></span>                                                    |
| <span data-ttu-id="1efa2-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1efa2-178">Range-Upper</span></span>            | <span data-ttu-id="1efa2-179">31557600</span><span class="sxs-lookup"><span data-stu-id="1efa2-179">31557600</span></span>                                             |
| <span data-ttu-id="1efa2-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa2-180">Search-Flags</span></span>           | <span data-ttu-id="1efa2-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1efa2-181">0x00000000</span></span>                                           |
| <span data-ttu-id="1efa2-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa2-182">System-Flags</span></span>           | <span data-ttu-id="1efa2-183">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1efa2-183">0x00000014</span></span>                                           |
| <span data-ttu-id="1efa2-184">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1efa2-184">Classes used in</span></span>        | [<span data-ttu-id="1efa2-185">**Dynamic-Object**</span><span class="sxs-lookup"><span data-stu-id="1efa2-185">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1efa2-186">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1efa2-186">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1efa2-187">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1efa2-187">Entry</span></span> | <span data-ttu-id="1efa2-188">Wert</span><span class="sxs-lookup"><span data-stu-id="1efa2-188">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1efa2-189">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1efa2-189">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1efa2-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1efa2-190">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1efa2-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="1efa2-191">System-Only</span></span>            | <span data-ttu-id="1efa2-192">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-192">False</span></span>                                                |
| <span data-ttu-id="1efa2-193">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1efa2-193">Is-Single-Valued</span></span>       | <span data-ttu-id="1efa2-194">Richtig</span><span class="sxs-lookup"><span data-stu-id="1efa2-194">True</span></span>                                                 |
| <span data-ttu-id="1efa2-195">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1efa2-195">Is Indexed</span></span>             | <span data-ttu-id="1efa2-196">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-196">False</span></span>                                                |
| <span data-ttu-id="1efa2-197">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1efa2-197">In Global Catalog</span></span>      | <span data-ttu-id="1efa2-198">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-198">False</span></span>                                                |
| <span data-ttu-id="1efa2-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1efa2-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="1efa2-200">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1efa2-200">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1efa2-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1efa2-201">Range-Lower</span></span>            | <span data-ttu-id="1efa2-202">0</span><span class="sxs-lookup"><span data-stu-id="1efa2-202">0</span></span>                                                    |
| <span data-ttu-id="1efa2-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1efa2-203">Range-Upper</span></span>            | <span data-ttu-id="1efa2-204">31557600</span><span class="sxs-lookup"><span data-stu-id="1efa2-204">31557600</span></span>                                             |
| <span data-ttu-id="1efa2-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa2-205">Search-Flags</span></span>           | <span data-ttu-id="1efa2-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1efa2-206">0x00000000</span></span>                                           |
| <span data-ttu-id="1efa2-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa2-207">System-Flags</span></span>           | <span data-ttu-id="1efa2-208">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1efa2-208">0x00000014</span></span>                                           |
| <span data-ttu-id="1efa2-209">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1efa2-209">Classes used in</span></span>        | [<span data-ttu-id="1efa2-210">**Dynamic-Object**</span><span class="sxs-lookup"><span data-stu-id="1efa2-210">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1efa2-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1efa2-211">Windows Server 2008</span></span>



| <span data-ttu-id="1efa2-212">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1efa2-212">Entry</span></span> | <span data-ttu-id="1efa2-213">Wert</span><span class="sxs-lookup"><span data-stu-id="1efa2-213">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1efa2-214">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1efa2-214">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1efa2-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1efa2-215">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1efa2-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="1efa2-216">System-Only</span></span>            | <span data-ttu-id="1efa2-217">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-217">False</span></span>                                                |
| <span data-ttu-id="1efa2-218">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1efa2-218">Is-Single-Valued</span></span>       | <span data-ttu-id="1efa2-219">Richtig</span><span class="sxs-lookup"><span data-stu-id="1efa2-219">True</span></span>                                                 |
| <span data-ttu-id="1efa2-220">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1efa2-220">Is Indexed</span></span>             | <span data-ttu-id="1efa2-221">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-221">False</span></span>                                                |
| <span data-ttu-id="1efa2-222">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1efa2-222">In Global Catalog</span></span>      | <span data-ttu-id="1efa2-223">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-223">False</span></span>                                                |
| <span data-ttu-id="1efa2-224">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1efa2-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="1efa2-225">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1efa2-225">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1efa2-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1efa2-226">Range-Lower</span></span>            | <span data-ttu-id="1efa2-227">0</span><span class="sxs-lookup"><span data-stu-id="1efa2-227">0</span></span>                                                    |
| <span data-ttu-id="1efa2-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1efa2-228">Range-Upper</span></span>            | <span data-ttu-id="1efa2-229">31557600</span><span class="sxs-lookup"><span data-stu-id="1efa2-229">31557600</span></span>                                             |
| <span data-ttu-id="1efa2-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa2-230">Search-Flags</span></span>           | <span data-ttu-id="1efa2-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1efa2-231">0x00000000</span></span>                                           |
| <span data-ttu-id="1efa2-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa2-232">System-Flags</span></span>           | <span data-ttu-id="1efa2-233">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1efa2-233">0x00000014</span></span>                                           |
| <span data-ttu-id="1efa2-234">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1efa2-234">Classes used in</span></span>        | [<span data-ttu-id="1efa2-235">**Dynamic-Object**</span><span class="sxs-lookup"><span data-stu-id="1efa2-235">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1efa2-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1efa2-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1efa2-237">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1efa2-237">Entry</span></span> | <span data-ttu-id="1efa2-238">Wert</span><span class="sxs-lookup"><span data-stu-id="1efa2-238">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1efa2-239">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1efa2-239">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1efa2-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1efa2-240">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1efa2-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="1efa2-241">System-Only</span></span>            | <span data-ttu-id="1efa2-242">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-242">False</span></span>                                                |
| <span data-ttu-id="1efa2-243">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1efa2-243">Is-Single-Valued</span></span>       | <span data-ttu-id="1efa2-244">Richtig</span><span class="sxs-lookup"><span data-stu-id="1efa2-244">True</span></span>                                                 |
| <span data-ttu-id="1efa2-245">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1efa2-245">Is Indexed</span></span>             | <span data-ttu-id="1efa2-246">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-246">False</span></span>                                                |
| <span data-ttu-id="1efa2-247">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1efa2-247">In Global Catalog</span></span>      | <span data-ttu-id="1efa2-248">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-248">False</span></span>                                                |
| <span data-ttu-id="1efa2-249">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1efa2-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="1efa2-250">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1efa2-250">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1efa2-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1efa2-251">Range-Lower</span></span>            | <span data-ttu-id="1efa2-252">0</span><span class="sxs-lookup"><span data-stu-id="1efa2-252">0</span></span>                                                    |
| <span data-ttu-id="1efa2-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1efa2-253">Range-Upper</span></span>            | <span data-ttu-id="1efa2-254">31557600</span><span class="sxs-lookup"><span data-stu-id="1efa2-254">31557600</span></span>                                             |
| <span data-ttu-id="1efa2-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa2-255">Search-Flags</span></span>           | <span data-ttu-id="1efa2-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1efa2-256">0x00000000</span></span>                                           |
| <span data-ttu-id="1efa2-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa2-257">System-Flags</span></span>           | <span data-ttu-id="1efa2-258">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1efa2-258">0x00000014</span></span>                                           |
| <span data-ttu-id="1efa2-259">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1efa2-259">Classes used in</span></span>        | [<span data-ttu-id="1efa2-260">**Dynamic-Object**</span><span class="sxs-lookup"><span data-stu-id="1efa2-260">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1efa2-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1efa2-261">Windows Server 2012</span></span>



| <span data-ttu-id="1efa2-262">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1efa2-262">Entry</span></span> | <span data-ttu-id="1efa2-263">Wert</span><span class="sxs-lookup"><span data-stu-id="1efa2-263">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1efa2-264">Link-ID</span><span class="sxs-lookup"><span data-stu-id="1efa2-264">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1efa2-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1efa2-265">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1efa2-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="1efa2-266">System-Only</span></span>            | <span data-ttu-id="1efa2-267">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-267">False</span></span>                                                |
| <span data-ttu-id="1efa2-268">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="1efa2-268">Is-Single-Valued</span></span>       | <span data-ttu-id="1efa2-269">Richtig</span><span class="sxs-lookup"><span data-stu-id="1efa2-269">True</span></span>                                                 |
| <span data-ttu-id="1efa2-270">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="1efa2-270">Is Indexed</span></span>             | <span data-ttu-id="1efa2-271">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-271">False</span></span>                                                |
| <span data-ttu-id="1efa2-272">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="1efa2-272">In Global Catalog</span></span>      | <span data-ttu-id="1efa2-273">False</span><span class="sxs-lookup"><span data-stu-id="1efa2-273">False</span></span>                                                |
| <span data-ttu-id="1efa2-274">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1efa2-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="1efa2-275">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="1efa2-275">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1efa2-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1efa2-276">Range-Lower</span></span>            | <span data-ttu-id="1efa2-277">0</span><span class="sxs-lookup"><span data-stu-id="1efa2-277">0</span></span>                                                    |
| <span data-ttu-id="1efa2-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1efa2-278">Range-Upper</span></span>            | <span data-ttu-id="1efa2-279">31557600</span><span class="sxs-lookup"><span data-stu-id="1efa2-279">31557600</span></span>                                             |
| <span data-ttu-id="1efa2-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa2-280">Search-Flags</span></span>           | <span data-ttu-id="1efa2-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1efa2-281">0x00000000</span></span>                                           |
| <span data-ttu-id="1efa2-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1efa2-282">System-Flags</span></span>           | <span data-ttu-id="1efa2-283">0x00000014</span><span class="sxs-lookup"><span data-stu-id="1efa2-283">0x00000014</span></span>                                           |
| <span data-ttu-id="1efa2-284">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="1efa2-284">Classes used in</span></span>        | [<span data-ttu-id="1efa2-285">**Dynamic-Object**</span><span class="sxs-lookup"><span data-stu-id="1efa2-285">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



 

 





