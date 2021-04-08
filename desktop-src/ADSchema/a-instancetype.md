---
title: Instance-Type-Attribut
description: Ein Bitfeld, das festlegt, wie das-Objekt auf einem bestimmten Server instanziiert wird.
ms.assetid: ed77c302-3d80-4292-8e48-bfc6cb5079ee
ms.tgt_platform: multiple
keywords:
- AD-Schema für Instance-Type-Attribut
- AD-Schema des instanceType-Attributs
topic_type:
- apiref
api_name:
- Instance-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e31eec3c5a7a189f4623e8e77badb3b1e83e0cd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744833"
---
# <a name="instance-type-attribute"></a><span data-ttu-id="8b102-105">Instance-Type-Attribut</span><span class="sxs-lookup"><span data-stu-id="8b102-105">Instance-Type attribute</span></span>

<span data-ttu-id="8b102-106">Ein Bitfeld, das festlegt, wie das-Objekt auf einem bestimmten Server instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="8b102-106">A bitfield that dictates how the object is instantiated on a particular server.</span></span> <span data-ttu-id="8b102-107">Der Wert dieses Attributs kann sich bei verschiedenen Replikaten auch dann unterscheiden, wenn die Replikate synchronisiert sind.</span><span class="sxs-lookup"><span data-stu-id="8b102-107">The value of this attribute can differ on different replicas even if the replicas are in sync.</span></span>

<span data-ttu-id="8b102-108">Dieses Attribut kann NULL sein oder eine Kombination aus einem oder mehreren der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8b102-108">This attribute can be zero or a combination of one or more of the following values.</span></span>

| <span data-ttu-id="8b102-109">Wert</span><span class="sxs-lookup"><span data-stu-id="8b102-109">Value</span></span>      | <span data-ttu-id="8b102-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b102-110">Description</span></span>                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b102-111">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8b102-111">0x00000001</span></span> | <span data-ttu-id="8b102-112">Die Kopfzeile des Namens Kontexts.</span><span class="sxs-lookup"><span data-stu-id="8b102-112">The head of naming context.</span></span>                                                                        |
| <span data-ttu-id="8b102-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8b102-113">0x00000002</span></span> | <span data-ttu-id="8b102-114">Dieses Replikat wird nicht instanziiert.</span><span class="sxs-lookup"><span data-stu-id="8b102-114">This replica is not instantiated.</span></span>                                                                  |
| <span data-ttu-id="8b102-115">0x00000004</span><span class="sxs-lookup"><span data-stu-id="8b102-115">0x00000004</span></span> | <span data-ttu-id="8b102-116">Das Objekt ist in diesem Verzeichnis beschreibbar.</span><span class="sxs-lookup"><span data-stu-id="8b102-116">The object is writable on this directory.</span></span>                                                          |
| <span data-ttu-id="8b102-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8b102-117">0x00000008</span></span> | <span data-ttu-id="8b102-118">Der namens Kontext für dieses Verzeichnis wird in diesem Verzeichnis gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8b102-118">The naming context above this one on this directory is held.</span></span>                                       |
| <span data-ttu-id="8b102-119">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b102-119">0x00000010</span></span> | <span data-ttu-id="8b102-120">Der namens Kontext wird zum ersten Mal mithilfe der Replikation erstellt.</span><span class="sxs-lookup"><span data-stu-id="8b102-120">The naming context is in the process of being constructed for the first time by using replication.</span></span> |
| <span data-ttu-id="8b102-121">0x00000020</span><span class="sxs-lookup"><span data-stu-id="8b102-121">0x00000020</span></span> | <span data-ttu-id="8b102-122">Der namens Kontext wird gerade aus dem lokalen DSA entfernt.</span><span class="sxs-lookup"><span data-stu-id="8b102-122">The naming context is in the process of being removed from the local DSA.</span></span>                          |



 



| <span data-ttu-id="8b102-123">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8b102-123">Entry</span></span> | <span data-ttu-id="8b102-124">Wert</span><span class="sxs-lookup"><span data-stu-id="8b102-124">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="8b102-125">CN</span><span class="sxs-lookup"><span data-stu-id="8b102-125">CN</span></span>                | <span data-ttu-id="8b102-126">Instance-Type</span><span class="sxs-lookup"><span data-stu-id="8b102-126">Instance-Type</span></span>                                  |
| <span data-ttu-id="8b102-127">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8b102-127">Ldap-Display-Name</span></span> | <span data-ttu-id="8b102-128">instanceType</span><span class="sxs-lookup"><span data-stu-id="8b102-128">instanceType</span></span>                                   |
| <span data-ttu-id="8b102-129">Size</span><span class="sxs-lookup"><span data-stu-id="8b102-129">Size</span></span>              | <span data-ttu-id="8b102-130">4 Bytes.</span><span class="sxs-lookup"><span data-stu-id="8b102-130">4 bytes.</span></span>                                       |
| <span data-ttu-id="8b102-131">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="8b102-131">Update Privilege</span></span>  | <span data-ttu-id="8b102-132">Dieser Wert wird vom Schema Administrator festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8b102-132">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="8b102-133">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="8b102-133">Update Frequency</span></span>  | <span data-ttu-id="8b102-134">Wenn das Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8b102-134">When the object is created.</span></span>                    |
| <span data-ttu-id="8b102-135">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8b102-135">Attribute-Id</span></span>      | <span data-ttu-id="8b102-136">1.2.840.113556.1.2.1</span><span class="sxs-lookup"><span data-stu-id="8b102-136">1.2.840.113556.1.2.1</span></span>                           |
| <span data-ttu-id="8b102-137">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8b102-137">System-Id-Guid</span></span>    | <span data-ttu-id="8b102-138">bf96798c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8b102-138">bf96798c-0de6-11d0-a285-00aa003049e2</span></span>           |
| <span data-ttu-id="8b102-139">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b102-139">Syntax</span></span>            | [<span data-ttu-id="8b102-140">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="8b102-140">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="8b102-141">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="8b102-141">Implementations</span></span>

-   [<span data-ttu-id="8b102-142">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8b102-142">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8b102-143">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8b102-143">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8b102-144">**Adam**</span><span class="sxs-lookup"><span data-stu-id="8b102-144">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8b102-145">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8b102-145">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8b102-146">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8b102-146">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8b102-147">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8b102-147">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8b102-148">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8b102-148">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8b102-149">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8b102-149">Windows 2000 Server</span></span>



| <span data-ttu-id="8b102-150">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8b102-150">Entry</span></span> | <span data-ttu-id="8b102-151">Wert</span><span class="sxs-lookup"><span data-stu-id="8b102-151">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8b102-152">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8b102-152">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8b102-153">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b102-153">MAPI-Id</span></span>                | <span data-ttu-id="8b102-154">0x80bd</span><span class="sxs-lookup"><span data-stu-id="8b102-154">0x80BD</span></span>                          |
| <span data-ttu-id="8b102-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b102-155">System-Only</span></span>            | <span data-ttu-id="8b102-156">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-156">True</span></span>                            |
| <span data-ttu-id="8b102-157">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8b102-157">Is-Single-Valued</span></span>       | <span data-ttu-id="8b102-158">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-158">True</span></span>                            |
| <span data-ttu-id="8b102-159">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8b102-159">Is Indexed</span></span>             | <span data-ttu-id="8b102-160">False</span><span class="sxs-lookup"><span data-stu-id="8b102-160">False</span></span>                           |
| <span data-ttu-id="8b102-161">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8b102-161">In Global Catalog</span></span>      | <span data-ttu-id="8b102-162">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-162">True</span></span>                            |
| <span data-ttu-id="8b102-163">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8b102-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b102-164">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8b102-164">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8b102-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b102-165">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8b102-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b102-166">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8b102-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b102-167">Search-Flags</span></span>           | <span data-ttu-id="8b102-168">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8b102-168">0x00000008</span></span>                      |
| <span data-ttu-id="8b102-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b102-169">System-Flags</span></span>           | <span data-ttu-id="8b102-170">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8b102-170">0x00000012</span></span>                      |
| <span data-ttu-id="8b102-171">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8b102-171">Classes used in</span></span>        | [<span data-ttu-id="8b102-172">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="8b102-172">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8b102-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8b102-173">Windows Server 2003</span></span>



| <span data-ttu-id="8b102-174">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8b102-174">Entry</span></span> | <span data-ttu-id="8b102-175">Wert</span><span class="sxs-lookup"><span data-stu-id="8b102-175">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8b102-176">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8b102-176">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8b102-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b102-177">MAPI-Id</span></span>                | <span data-ttu-id="8b102-178">0x80bd</span><span class="sxs-lookup"><span data-stu-id="8b102-178">0x80BD</span></span>                          |
| <span data-ttu-id="8b102-179">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b102-179">System-Only</span></span>            | <span data-ttu-id="8b102-180">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-180">True</span></span>                            |
| <span data-ttu-id="8b102-181">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8b102-181">Is-Single-Valued</span></span>       | <span data-ttu-id="8b102-182">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-182">True</span></span>                            |
| <span data-ttu-id="8b102-183">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8b102-183">Is Indexed</span></span>             | <span data-ttu-id="8b102-184">False</span><span class="sxs-lookup"><span data-stu-id="8b102-184">False</span></span>                           |
| <span data-ttu-id="8b102-185">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8b102-185">In Global Catalog</span></span>      | <span data-ttu-id="8b102-186">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-186">True</span></span>                            |
| <span data-ttu-id="8b102-187">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8b102-187">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b102-188">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8b102-188">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8b102-189">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b102-189">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8b102-190">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b102-190">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8b102-191">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b102-191">Search-Flags</span></span>           | <span data-ttu-id="8b102-192">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8b102-192">0x00000008</span></span>                      |
| <span data-ttu-id="8b102-193">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b102-193">System-Flags</span></span>           | <span data-ttu-id="8b102-194">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8b102-194">0x00000012</span></span>                      |
| <span data-ttu-id="8b102-195">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8b102-195">Classes used in</span></span>        | [<span data-ttu-id="8b102-196">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="8b102-196">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8b102-197">Adam</span><span class="sxs-lookup"><span data-stu-id="8b102-197">ADAM</span></span>



| <span data-ttu-id="8b102-198">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8b102-198">Entry</span></span> | <span data-ttu-id="8b102-199">Wert</span><span class="sxs-lookup"><span data-stu-id="8b102-199">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8b102-200">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8b102-200">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8b102-201">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b102-201">MAPI-Id</span></span>                | <span data-ttu-id="8b102-202">0x80bd</span><span class="sxs-lookup"><span data-stu-id="8b102-202">0x80BD</span></span>                          |
| <span data-ttu-id="8b102-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b102-203">System-Only</span></span>            | <span data-ttu-id="8b102-204">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-204">True</span></span>                            |
| <span data-ttu-id="8b102-205">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8b102-205">Is-Single-Valued</span></span>       | <span data-ttu-id="8b102-206">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-206">True</span></span>                            |
| <span data-ttu-id="8b102-207">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8b102-207">Is Indexed</span></span>             | <span data-ttu-id="8b102-208">False</span><span class="sxs-lookup"><span data-stu-id="8b102-208">False</span></span>                           |
| <span data-ttu-id="8b102-209">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8b102-209">In Global Catalog</span></span>      | <span data-ttu-id="8b102-210">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-210">True</span></span>                            |
| <span data-ttu-id="8b102-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8b102-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b102-212">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8b102-212">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8b102-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b102-213">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8b102-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b102-214">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8b102-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b102-215">Search-Flags</span></span>           | <span data-ttu-id="8b102-216">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8b102-216">0x00000008</span></span>                      |
| <span data-ttu-id="8b102-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b102-217">System-Flags</span></span>           | <span data-ttu-id="8b102-218">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8b102-218">0x00000012</span></span>                      |
| <span data-ttu-id="8b102-219">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8b102-219">Classes used in</span></span>        | [<span data-ttu-id="8b102-220">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="8b102-220">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8b102-221">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8b102-221">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8b102-222">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8b102-222">Entry</span></span> | <span data-ttu-id="8b102-223">Wert</span><span class="sxs-lookup"><span data-stu-id="8b102-223">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8b102-224">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8b102-224">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8b102-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b102-225">MAPI-Id</span></span>                | <span data-ttu-id="8b102-226">0x80bd</span><span class="sxs-lookup"><span data-stu-id="8b102-226">0x80BD</span></span>                          |
| <span data-ttu-id="8b102-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b102-227">System-Only</span></span>            | <span data-ttu-id="8b102-228">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-228">True</span></span>                            |
| <span data-ttu-id="8b102-229">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8b102-229">Is-Single-Valued</span></span>       | <span data-ttu-id="8b102-230">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-230">True</span></span>                            |
| <span data-ttu-id="8b102-231">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8b102-231">Is Indexed</span></span>             | <span data-ttu-id="8b102-232">False</span><span class="sxs-lookup"><span data-stu-id="8b102-232">False</span></span>                           |
| <span data-ttu-id="8b102-233">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8b102-233">In Global Catalog</span></span>      | <span data-ttu-id="8b102-234">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-234">True</span></span>                            |
| <span data-ttu-id="8b102-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8b102-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b102-236">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8b102-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8b102-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b102-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8b102-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b102-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8b102-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b102-239">Search-Flags</span></span>           | <span data-ttu-id="8b102-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8b102-240">0x00000008</span></span>                      |
| <span data-ttu-id="8b102-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b102-241">System-Flags</span></span>           | <span data-ttu-id="8b102-242">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8b102-242">0x00000012</span></span>                      |
| <span data-ttu-id="8b102-243">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8b102-243">Classes used in</span></span>        | [<span data-ttu-id="8b102-244">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="8b102-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8b102-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b102-245">Windows Server 2008</span></span>



| <span data-ttu-id="8b102-246">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8b102-246">Entry</span></span> | <span data-ttu-id="8b102-247">Wert</span><span class="sxs-lookup"><span data-stu-id="8b102-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8b102-248">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8b102-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8b102-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b102-249">MAPI-Id</span></span>                | <span data-ttu-id="8b102-250">0x80bd</span><span class="sxs-lookup"><span data-stu-id="8b102-250">0x80BD</span></span>                          |
| <span data-ttu-id="8b102-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b102-251">System-Only</span></span>            | <span data-ttu-id="8b102-252">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-252">True</span></span>                            |
| <span data-ttu-id="8b102-253">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8b102-253">Is-Single-Valued</span></span>       | <span data-ttu-id="8b102-254">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-254">True</span></span>                            |
| <span data-ttu-id="8b102-255">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8b102-255">Is Indexed</span></span>             | <span data-ttu-id="8b102-256">False</span><span class="sxs-lookup"><span data-stu-id="8b102-256">False</span></span>                           |
| <span data-ttu-id="8b102-257">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8b102-257">In Global Catalog</span></span>      | <span data-ttu-id="8b102-258">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-258">True</span></span>                            |
| <span data-ttu-id="8b102-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8b102-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b102-260">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8b102-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8b102-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b102-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8b102-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b102-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8b102-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b102-263">Search-Flags</span></span>           | <span data-ttu-id="8b102-264">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8b102-264">0x00000008</span></span>                      |
| <span data-ttu-id="8b102-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b102-265">System-Flags</span></span>           | <span data-ttu-id="8b102-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8b102-266">0x00000012</span></span>                      |
| <span data-ttu-id="8b102-267">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8b102-267">Classes used in</span></span>        | [<span data-ttu-id="8b102-268">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="8b102-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8b102-269">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8b102-269">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8b102-270">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8b102-270">Entry</span></span> | <span data-ttu-id="8b102-271">Wert</span><span class="sxs-lookup"><span data-stu-id="8b102-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8b102-272">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8b102-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8b102-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b102-273">MAPI-Id</span></span>                | <span data-ttu-id="8b102-274">0x80bd</span><span class="sxs-lookup"><span data-stu-id="8b102-274">0x80BD</span></span>                          |
| <span data-ttu-id="8b102-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b102-275">System-Only</span></span>            | <span data-ttu-id="8b102-276">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-276">True</span></span>                            |
| <span data-ttu-id="8b102-277">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8b102-277">Is-Single-Valued</span></span>       | <span data-ttu-id="8b102-278">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-278">True</span></span>                            |
| <span data-ttu-id="8b102-279">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8b102-279">Is Indexed</span></span>             | <span data-ttu-id="8b102-280">False</span><span class="sxs-lookup"><span data-stu-id="8b102-280">False</span></span>                           |
| <span data-ttu-id="8b102-281">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8b102-281">In Global Catalog</span></span>      | <span data-ttu-id="8b102-282">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-282">True</span></span>                            |
| <span data-ttu-id="8b102-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8b102-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b102-284">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8b102-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8b102-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b102-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8b102-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b102-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8b102-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b102-287">Search-Flags</span></span>           | <span data-ttu-id="8b102-288">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8b102-288">0x00000008</span></span>                      |
| <span data-ttu-id="8b102-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b102-289">System-Flags</span></span>           | <span data-ttu-id="8b102-290">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8b102-290">0x00000012</span></span>                      |
| <span data-ttu-id="8b102-291">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8b102-291">Classes used in</span></span>        | [<span data-ttu-id="8b102-292">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="8b102-292">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8b102-293">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8b102-293">Windows Server 2012</span></span>



| <span data-ttu-id="8b102-294">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8b102-294">Entry</span></span> | <span data-ttu-id="8b102-295">Wert</span><span class="sxs-lookup"><span data-stu-id="8b102-295">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8b102-296">Link-ID</span><span class="sxs-lookup"><span data-stu-id="8b102-296">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8b102-297">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b102-297">MAPI-Id</span></span>                | <span data-ttu-id="8b102-298">0x80bd</span><span class="sxs-lookup"><span data-stu-id="8b102-298">0x80BD</span></span>                          |
| <span data-ttu-id="8b102-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b102-299">System-Only</span></span>            | <span data-ttu-id="8b102-300">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-300">True</span></span>                            |
| <span data-ttu-id="8b102-301">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="8b102-301">Is-Single-Valued</span></span>       | <span data-ttu-id="8b102-302">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-302">True</span></span>                            |
| <span data-ttu-id="8b102-303">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="8b102-303">Is Indexed</span></span>             | <span data-ttu-id="8b102-304">False</span><span class="sxs-lookup"><span data-stu-id="8b102-304">False</span></span>                           |
| <span data-ttu-id="8b102-305">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="8b102-305">In Global Catalog</span></span>      | <span data-ttu-id="8b102-306">Richtig</span><span class="sxs-lookup"><span data-stu-id="8b102-306">True</span></span>                            |
| <span data-ttu-id="8b102-307">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8b102-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b102-308">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="8b102-308">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8b102-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b102-309">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8b102-310">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b102-310">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8b102-311">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b102-311">Search-Flags</span></span>           | <span data-ttu-id="8b102-312">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8b102-312">0x00000008</span></span>                      |
| <span data-ttu-id="8b102-313">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b102-313">System-Flags</span></span>           | <span data-ttu-id="8b102-314">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8b102-314">0x00000012</span></span>                      |
| <span data-ttu-id="8b102-315">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="8b102-315">Classes used in</span></span>        | [<span data-ttu-id="8b102-316">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="8b102-316">**Top**</span></span>](c-top.md)<br/> |



 

 





