---
title: Well-Known-Objects-Attribut
description: Dieses Attribut enthält eine Liste bekannter Objekt Container nach GUID und Distinguished Name.
ms.assetid: e3c2d243-6734-4c2f-9ead-bc4ec071d1f1
ms.tgt_platform: multiple
keywords:
- Well-Known-Objects-Attribut AD-Schema
- wellKnownObjects-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e21df3db14a29de137af4792f0e9ca6df27b90
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480199"
---
# <a name="well-known-objects-attribute"></a><span data-ttu-id="f3bd1-105">Well-Known-Objects-Attribut</span><span class="sxs-lookup"><span data-stu-id="f3bd1-105">Well-Known-Objects attribute</span></span>

<span data-ttu-id="f3bd1-106">Dieses Attribut enthält eine Liste bekannter Objekt Container nach GUID und Distinguished Name.</span><span class="sxs-lookup"><span data-stu-id="f3bd1-106">This attribute contains a list of well-known object containers by GUID and distinguished name.</span></span> <span data-ttu-id="f3bd1-107">Bei den bekannten Objekten handelt es sich um System Container.</span><span class="sxs-lookup"><span data-stu-id="f3bd1-107">The well-known objects are system containers.</span></span> <span data-ttu-id="f3bd1-108">Diese Informationen werden verwendet, um ein Objekt abzurufen, nachdem es mit nur der GUID und dem Domänen Namen verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="f3bd1-108">This information is used to retrieve an object after it has been moved by using just the GUID and the domain name.</span></span> <span data-ttu-id="f3bd1-109">Wenn das-Objekt verschoben wird, aktualisiert das System automatisch den Distinguished Name-Teil der Well-Known Objects-Werte, die auf das-Objekt verwiesen haben.</span><span class="sxs-lookup"><span data-stu-id="f3bd1-109">Whenever the object is moved, the system automatically updates the Distinguished Name portion of the Well-Known-Objects values that referred to the object.</span></span> <span data-ttu-id="f3bd1-110">Die Datei NTDSAPI. h enthält die folgenden Definitionen, die zum Abrufen eines Objekts verwendet werden können (die GUIDs, die diesen Objekten zugeordnet sind, sind in NTDSAPI. h enthalten):</span><span class="sxs-lookup"><span data-stu-id="f3bd1-110">The file Ntdsapi.h contains the following definitions, which can be used to retrieve an object (the GUIDs that are associated to these objects are contained in Ntdsapi.h):</span></span>

-   <span data-ttu-id="f3bd1-111">GUID- \_ Benutzer \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="f3bd1-111">GUID\_USERS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="f3bd1-112">GUID- \_ computrs- \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="f3bd1-112">GUID\_COMPUTRS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="f3bd1-113">GUID- \_ Systeme \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="f3bd1-113">GUID\_SYSTEMS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="f3bd1-114">GUID- \_ Domänen \_ Controller \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="f3bd1-114">GUID\_DOMAIN\_CONTROLLERS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="f3bd1-115">GUID- \_ Infrastruktur \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="f3bd1-115">GUID\_INFRASTRUCTURE\_CONTAINER\_W</span></span>
-   <span data-ttu-id="f3bd1-116">GUID- \_ Gelöschte \_ Objekte \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="f3bd1-116">GUID\_DELETED\_OBJECTS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="f3bd1-117">GUID \_ LostAndFound- \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="f3bd1-117">GUID\_LOSTANDFOUND\_CONTAINER\_W</span></span>
-   <span data-ttu-id="f3bd1-118">GUID fremd \_ nsecurityprincipals \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="f3bd1-118">GUID\_FOREIGNSECURITYPRINCIPALS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="f3bd1-119">GUID- \_ Programm \_ Daten \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="f3bd1-119">GUID\_PROGRAM\_DATA\_CONTAINER\_W</span></span>
-   <span data-ttu-id="f3bd1-120">GUID \_ Microsoft- \_ Programm \_ Daten \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="f3bd1-120">GUID\_MICROSOFT\_PROGRAM\_DATA\_CONTAINER\_W</span></span>
-   <span data-ttu-id="f3bd1-121">GUID \_ NTDS- \_ Kontingente \_ Container \_ W</span><span class="sxs-lookup"><span data-stu-id="f3bd1-121">GUID\_NTDS\_QUOTAS\_CONTAINER\_W</span></span>



| <span data-ttu-id="f3bd1-122">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f3bd1-122">Entry</span></span> | <span data-ttu-id="f3bd1-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f3bd1-123">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="f3bd1-124">CN</span><span class="sxs-lookup"><span data-stu-id="f3bd1-124">CN</span></span>                | <span data-ttu-id="f3bd1-125">Bekannte Objekte</span><span class="sxs-lookup"><span data-stu-id="f3bd1-125">Well-Known-Objects</span></span>                              |
| <span data-ttu-id="f3bd1-126">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f3bd1-126">Ldap-Display-Name</span></span> | <span data-ttu-id="f3bd1-127">wellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="f3bd1-127">wellKnownObjects</span></span>                                |
| <span data-ttu-id="f3bd1-128">Size</span><span class="sxs-lookup"><span data-stu-id="f3bd1-128">Size</span></span>              | \-                                              |
| <span data-ttu-id="f3bd1-129">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f3bd1-129">Update Privilege</span></span>  | <span data-ttu-id="f3bd1-130">Dieser Wert wird vom System festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f3bd1-130">This value is set by the system.</span></span>                |
| <span data-ttu-id="f3bd1-131">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f3bd1-131">Update Frequency</span></span>  | <span data-ttu-id="f3bd1-132">Jedes Mal, wenn einer der System Container verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="f3bd1-132">Whenever one of the system containers is moved.</span></span> |
| <span data-ttu-id="f3bd1-133">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f3bd1-133">Attribute-Id</span></span>      | <span data-ttu-id="f3bd1-134">1.2.840.113556.1.4.618</span><span class="sxs-lookup"><span data-stu-id="f3bd1-134">1.2.840.113556.1.4.618</span></span>                          |
| <span data-ttu-id="f3bd1-135">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f3bd1-135">System-Id-Guid</span></span>    | <span data-ttu-id="f3bd1-136">05308983-7688-11d1-aded-00c04f d8d5cd</span><span class="sxs-lookup"><span data-stu-id="f3bd1-136">05308983-7688-11d1-aded-00c04fd8d5cd</span></span>            |
| <span data-ttu-id="f3bd1-137">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3bd1-137">Syntax</span></span>            | [<span data-ttu-id="f3bd1-138">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="f3bd1-138">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="f3bd1-139">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f3bd1-139">Implementations</span></span>

-   [<span data-ttu-id="f3bd1-140">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f3bd1-140">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f3bd1-141">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f3bd1-141">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f3bd1-142">**Adam**</span><span class="sxs-lookup"><span data-stu-id="f3bd1-142">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f3bd1-143">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f3bd1-143">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f3bd1-144">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f3bd1-144">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f3bd1-145">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f3bd1-145">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f3bd1-146">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f3bd1-146">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f3bd1-147">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f3bd1-147">Windows 2000 Server</span></span>



| <span data-ttu-id="f3bd1-148">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f3bd1-148">Entry</span></span> | <span data-ttu-id="f3bd1-149">Wert</span><span class="sxs-lookup"><span data-stu-id="f3bd1-149">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3bd1-150">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f3bd1-150">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3bd1-151">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3bd1-151">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f3bd1-152">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3bd1-152">System-Only</span></span>            | <span data-ttu-id="f3bd1-153">Richtig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-153">True</span></span>                            |
| <span data-ttu-id="f3bd1-154">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-154">Is-Single-Valued</span></span>       | <span data-ttu-id="f3bd1-155">False</span><span class="sxs-lookup"><span data-stu-id="f3bd1-155">False</span></span>                           |
| <span data-ttu-id="f3bd1-156">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f3bd1-156">Is Indexed</span></span>             | <span data-ttu-id="f3bd1-157">False</span><span class="sxs-lookup"><span data-stu-id="f3bd1-157">False</span></span>                           |
| <span data-ttu-id="f3bd1-158">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f3bd1-158">In Global Catalog</span></span>      | <span data-ttu-id="f3bd1-159">Richtig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-159">True</span></span>                            |
| <span data-ttu-id="f3bd1-160">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3bd1-160">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3bd1-161">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f3bd1-161">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3bd1-162">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3bd1-162">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f3bd1-163">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3bd1-163">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f3bd1-164">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3bd1-164">Search-Flags</span></span>           | <span data-ttu-id="f3bd1-165">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3bd1-165">0x00000000</span></span>                      |
| <span data-ttu-id="f3bd1-166">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3bd1-166">System-Flags</span></span>           | <span data-ttu-id="f3bd1-167">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f3bd1-167">0x00000012</span></span>                      |
| <span data-ttu-id="f3bd1-168">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f3bd1-168">Classes used in</span></span>        | [<span data-ttu-id="f3bd1-169">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f3bd1-169">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f3bd1-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f3bd1-170">Windows Server 2003</span></span>



| <span data-ttu-id="f3bd1-171">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f3bd1-171">Entry</span></span> | <span data-ttu-id="f3bd1-172">Wert</span><span class="sxs-lookup"><span data-stu-id="f3bd1-172">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3bd1-173">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f3bd1-173">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3bd1-174">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3bd1-174">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f3bd1-175">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3bd1-175">System-Only</span></span>            | <span data-ttu-id="f3bd1-176">Richtig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-176">True</span></span>                            |
| <span data-ttu-id="f3bd1-177">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-177">Is-Single-Valued</span></span>       | <span data-ttu-id="f3bd1-178">False</span><span class="sxs-lookup"><span data-stu-id="f3bd1-178">False</span></span>                           |
| <span data-ttu-id="f3bd1-179">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f3bd1-179">Is Indexed</span></span>             | <span data-ttu-id="f3bd1-180">False</span><span class="sxs-lookup"><span data-stu-id="f3bd1-180">False</span></span>                           |
| <span data-ttu-id="f3bd1-181">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f3bd1-181">In Global Catalog</span></span>      | <span data-ttu-id="f3bd1-182">Richtig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-182">True</span></span>                            |
| <span data-ttu-id="f3bd1-183">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3bd1-183">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3bd1-184">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f3bd1-184">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3bd1-185">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3bd1-185">Range-Lower</span></span>            | <span data-ttu-id="f3bd1-186">16</span><span class="sxs-lookup"><span data-stu-id="f3bd1-186">16</span></span>                              |
| <span data-ttu-id="f3bd1-187">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3bd1-187">Range-Upper</span></span>            | <span data-ttu-id="f3bd1-188">16</span><span class="sxs-lookup"><span data-stu-id="f3bd1-188">16</span></span>                              |
| <span data-ttu-id="f3bd1-189">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3bd1-189">Search-Flags</span></span>           | <span data-ttu-id="f3bd1-190">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3bd1-190">0x00000000</span></span>                      |
| <span data-ttu-id="f3bd1-191">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3bd1-191">System-Flags</span></span>           | <span data-ttu-id="f3bd1-192">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f3bd1-192">0x00000012</span></span>                      |
| <span data-ttu-id="f3bd1-193">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f3bd1-193">Classes used in</span></span>        | [<span data-ttu-id="f3bd1-194">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f3bd1-194">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f3bd1-195">Adam</span><span class="sxs-lookup"><span data-stu-id="f3bd1-195">ADAM</span></span>



| <span data-ttu-id="f3bd1-196">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f3bd1-196">Entry</span></span> | <span data-ttu-id="f3bd1-197">Wert</span><span class="sxs-lookup"><span data-stu-id="f3bd1-197">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3bd1-198">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f3bd1-198">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3bd1-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3bd1-199">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f3bd1-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3bd1-200">System-Only</span></span>            | <span data-ttu-id="f3bd1-201">Richtig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-201">True</span></span>                            |
| <span data-ttu-id="f3bd1-202">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-202">Is-Single-Valued</span></span>       | <span data-ttu-id="f3bd1-203">False</span><span class="sxs-lookup"><span data-stu-id="f3bd1-203">False</span></span>                           |
| <span data-ttu-id="f3bd1-204">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f3bd1-204">Is Indexed</span></span>             | <span data-ttu-id="f3bd1-205">False</span><span class="sxs-lookup"><span data-stu-id="f3bd1-205">False</span></span>                           |
| <span data-ttu-id="f3bd1-206">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f3bd1-206">In Global Catalog</span></span>      | <span data-ttu-id="f3bd1-207">Richtig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-207">True</span></span>                            |
| <span data-ttu-id="f3bd1-208">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3bd1-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3bd1-209">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f3bd1-209">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3bd1-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3bd1-210">Range-Lower</span></span>            | <span data-ttu-id="f3bd1-211">16</span><span class="sxs-lookup"><span data-stu-id="f3bd1-211">16</span></span>                              |
| <span data-ttu-id="f3bd1-212">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3bd1-212">Range-Upper</span></span>            | <span data-ttu-id="f3bd1-213">16</span><span class="sxs-lookup"><span data-stu-id="f3bd1-213">16</span></span>                              |
| <span data-ttu-id="f3bd1-214">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3bd1-214">Search-Flags</span></span>           | <span data-ttu-id="f3bd1-215">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3bd1-215">0x00000000</span></span>                      |
| <span data-ttu-id="f3bd1-216">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3bd1-216">System-Flags</span></span>           | <span data-ttu-id="f3bd1-217">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f3bd1-217">0x00000012</span></span>                      |
| <span data-ttu-id="f3bd1-218">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f3bd1-218">Classes used in</span></span>        | [<span data-ttu-id="f3bd1-219">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f3bd1-219">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f3bd1-220">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f3bd1-220">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f3bd1-221">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f3bd1-221">Entry</span></span> | <span data-ttu-id="f3bd1-222">Wert</span><span class="sxs-lookup"><span data-stu-id="f3bd1-222">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3bd1-223">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f3bd1-223">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3bd1-224">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3bd1-224">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f3bd1-225">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3bd1-225">System-Only</span></span>            | <span data-ttu-id="f3bd1-226">Richtig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-226">True</span></span>                            |
| <span data-ttu-id="f3bd1-227">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-227">Is-Single-Valued</span></span>       | <span data-ttu-id="f3bd1-228">False</span><span class="sxs-lookup"><span data-stu-id="f3bd1-228">False</span></span>                           |
| <span data-ttu-id="f3bd1-229">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f3bd1-229">Is Indexed</span></span>             | <span data-ttu-id="f3bd1-230">False</span><span class="sxs-lookup"><span data-stu-id="f3bd1-230">False</span></span>                           |
| <span data-ttu-id="f3bd1-231">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f3bd1-231">In Global Catalog</span></span>      | <span data-ttu-id="f3bd1-232">Richtig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-232">True</span></span>                            |
| <span data-ttu-id="f3bd1-233">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3bd1-233">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3bd1-234">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f3bd1-234">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3bd1-235">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3bd1-235">Range-Lower</span></span>            | <span data-ttu-id="f3bd1-236">16</span><span class="sxs-lookup"><span data-stu-id="f3bd1-236">16</span></span>                              |
| <span data-ttu-id="f3bd1-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3bd1-237">Range-Upper</span></span>            | <span data-ttu-id="f3bd1-238">16</span><span class="sxs-lookup"><span data-stu-id="f3bd1-238">16</span></span>                              |
| <span data-ttu-id="f3bd1-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3bd1-239">Search-Flags</span></span>           | <span data-ttu-id="f3bd1-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3bd1-240">0x00000000</span></span>                      |
| <span data-ttu-id="f3bd1-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3bd1-241">System-Flags</span></span>           | <span data-ttu-id="f3bd1-242">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f3bd1-242">0x00000012</span></span>                      |
| <span data-ttu-id="f3bd1-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f3bd1-243">Classes used in</span></span>        | [<span data-ttu-id="f3bd1-244">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f3bd1-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f3bd1-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3bd1-245">Windows Server 2008</span></span>



| <span data-ttu-id="f3bd1-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f3bd1-246">Entry</span></span> | <span data-ttu-id="f3bd1-247">Wert</span><span class="sxs-lookup"><span data-stu-id="f3bd1-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3bd1-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f3bd1-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3bd1-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3bd1-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f3bd1-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3bd1-250">System-Only</span></span>            | <span data-ttu-id="f3bd1-251">Richtig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-251">True</span></span>                            |
| <span data-ttu-id="f3bd1-252">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-252">Is-Single-Valued</span></span>       | <span data-ttu-id="f3bd1-253">False</span><span class="sxs-lookup"><span data-stu-id="f3bd1-253">False</span></span>                           |
| <span data-ttu-id="f3bd1-254">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f3bd1-254">Is Indexed</span></span>             | <span data-ttu-id="f3bd1-255">False</span><span class="sxs-lookup"><span data-stu-id="f3bd1-255">False</span></span>                           |
| <span data-ttu-id="f3bd1-256">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f3bd1-256">In Global Catalog</span></span>      | <span data-ttu-id="f3bd1-257">Richtig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-257">True</span></span>                            |
| <span data-ttu-id="f3bd1-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3bd1-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3bd1-259">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f3bd1-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3bd1-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3bd1-260">Range-Lower</span></span>            | <span data-ttu-id="f3bd1-261">16</span><span class="sxs-lookup"><span data-stu-id="f3bd1-261">16</span></span>                              |
| <span data-ttu-id="f3bd1-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3bd1-262">Range-Upper</span></span>            | <span data-ttu-id="f3bd1-263">16</span><span class="sxs-lookup"><span data-stu-id="f3bd1-263">16</span></span>                              |
| <span data-ttu-id="f3bd1-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3bd1-264">Search-Flags</span></span>           | <span data-ttu-id="f3bd1-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3bd1-265">0x00000000</span></span>                      |
| <span data-ttu-id="f3bd1-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3bd1-266">System-Flags</span></span>           | <span data-ttu-id="f3bd1-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f3bd1-267">0x00000012</span></span>                      |
| <span data-ttu-id="f3bd1-268">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f3bd1-268">Classes used in</span></span>        | [<span data-ttu-id="f3bd1-269">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f3bd1-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f3bd1-270">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f3bd1-270">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f3bd1-271">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f3bd1-271">Entry</span></span> | <span data-ttu-id="f3bd1-272">Wert</span><span class="sxs-lookup"><span data-stu-id="f3bd1-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3bd1-273">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f3bd1-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3bd1-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3bd1-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f3bd1-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3bd1-275">System-Only</span></span>            | <span data-ttu-id="f3bd1-276">Richtig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-276">True</span></span>                            |
| <span data-ttu-id="f3bd1-277">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-277">Is-Single-Valued</span></span>       | <span data-ttu-id="f3bd1-278">False</span><span class="sxs-lookup"><span data-stu-id="f3bd1-278">False</span></span>                           |
| <span data-ttu-id="f3bd1-279">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f3bd1-279">Is Indexed</span></span>             | <span data-ttu-id="f3bd1-280">False</span><span class="sxs-lookup"><span data-stu-id="f3bd1-280">False</span></span>                           |
| <span data-ttu-id="f3bd1-281">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f3bd1-281">In Global Catalog</span></span>      | <span data-ttu-id="f3bd1-282">Richtig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-282">True</span></span>                            |
| <span data-ttu-id="f3bd1-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3bd1-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3bd1-284">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f3bd1-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3bd1-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3bd1-285">Range-Lower</span></span>            | <span data-ttu-id="f3bd1-286">16</span><span class="sxs-lookup"><span data-stu-id="f3bd1-286">16</span></span>                              |
| <span data-ttu-id="f3bd1-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3bd1-287">Range-Upper</span></span>            | <span data-ttu-id="f3bd1-288">16</span><span class="sxs-lookup"><span data-stu-id="f3bd1-288">16</span></span>                              |
| <span data-ttu-id="f3bd1-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3bd1-289">Search-Flags</span></span>           | <span data-ttu-id="f3bd1-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3bd1-290">0x00000000</span></span>                      |
| <span data-ttu-id="f3bd1-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3bd1-291">System-Flags</span></span>           | <span data-ttu-id="f3bd1-292">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f3bd1-292">0x00000012</span></span>                      |
| <span data-ttu-id="f3bd1-293">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f3bd1-293">Classes used in</span></span>        | [<span data-ttu-id="f3bd1-294">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f3bd1-294">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f3bd1-295">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f3bd1-295">Windows Server 2012</span></span>



| <span data-ttu-id="f3bd1-296">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f3bd1-296">Entry</span></span> | <span data-ttu-id="f3bd1-297">Wert</span><span class="sxs-lookup"><span data-stu-id="f3bd1-297">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f3bd1-298">Link-ID</span><span class="sxs-lookup"><span data-stu-id="f3bd1-298">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f3bd1-299">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3bd1-299">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f3bd1-300">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3bd1-300">System-Only</span></span>            | <span data-ttu-id="f3bd1-301">Richtig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-301">True</span></span>                            |
| <span data-ttu-id="f3bd1-302">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-302">Is-Single-Valued</span></span>       | <span data-ttu-id="f3bd1-303">False</span><span class="sxs-lookup"><span data-stu-id="f3bd1-303">False</span></span>                           |
| <span data-ttu-id="f3bd1-304">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="f3bd1-304">Is Indexed</span></span>             | <span data-ttu-id="f3bd1-305">False</span><span class="sxs-lookup"><span data-stu-id="f3bd1-305">False</span></span>                           |
| <span data-ttu-id="f3bd1-306">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="f3bd1-306">In Global Catalog</span></span>      | <span data-ttu-id="f3bd1-307">Richtig</span><span class="sxs-lookup"><span data-stu-id="f3bd1-307">True</span></span>                            |
| <span data-ttu-id="f3bd1-308">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3bd1-308">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3bd1-309">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="f3bd1-309">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f3bd1-310">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3bd1-310">Range-Lower</span></span>            | <span data-ttu-id="f3bd1-311">16</span><span class="sxs-lookup"><span data-stu-id="f3bd1-311">16</span></span>                              |
| <span data-ttu-id="f3bd1-312">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3bd1-312">Range-Upper</span></span>            | <span data-ttu-id="f3bd1-313">16</span><span class="sxs-lookup"><span data-stu-id="f3bd1-313">16</span></span>                              |
| <span data-ttu-id="f3bd1-314">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3bd1-314">Search-Flags</span></span>           | <span data-ttu-id="f3bd1-315">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3bd1-315">0x00000000</span></span>                      |
| <span data-ttu-id="f3bd1-316">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3bd1-316">System-Flags</span></span>           | <span data-ttu-id="f3bd1-317">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f3bd1-317">0x00000012</span></span>                      |
| <span data-ttu-id="f3bd1-318">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="f3bd1-318">Classes used in</span></span>        | [<span data-ttu-id="f3bd1-319">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="f3bd1-319">**Top**</span></span>](c-top.md)<br/> |



 

 





