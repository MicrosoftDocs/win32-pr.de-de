---
title: MS-IIS-FTP-dir-Attribut
description: Dieses Attribut bestimmt das Basisverzeichnis des Benutzers in Bezug auf die Dateiserver Freigabe. Sie wird in Verbindung mit MS-IIS-FTP-Root verwendet, um das Start Verzeichnis des FTP-Benutzers zu bestimmen.
ms.assetid: 99b22b79-1d42-440d-b92b-33bac3e811cb
ms.tgt_platform: multiple
keywords:
- MS-IIS-FTP-dir-Attribut AD-Schema
- AD-Schema des msIIS-FTPDir-Attributs
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Dir
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3067476e7dc275dbe14471d6c3c98fa5445a9dfe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519783"
---
# <a name="ms-iis-ftp-dir-attribute"></a><span data-ttu-id="c57ba-106">MS-IIS-FTP-dir-Attribut</span><span class="sxs-lookup"><span data-stu-id="c57ba-106">ms-IIS-FTP-Dir attribute</span></span>

<span data-ttu-id="c57ba-107">Dieses Attribut bestimmt das Basisverzeichnis des Benutzers in Bezug auf die Dateiserver Freigabe.</span><span class="sxs-lookup"><span data-stu-id="c57ba-107">This attribute determines the user home directory relative to the file server share.</span></span> <span data-ttu-id="c57ba-108">Sie wird in Verbindung mit MS-IIS-FTP-Root verwendet, um das Start Verzeichnis des FTP-Benutzers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="c57ba-108">It is used in conjunction with ms-IIS-FTP-Root to determine the FTP user home directory.</span></span>



| <span data-ttu-id="c57ba-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c57ba-109">Entry</span></span> | <span data-ttu-id="c57ba-110">Wert</span><span class="sxs-lookup"><span data-stu-id="c57ba-110">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c57ba-111">CN</span><span class="sxs-lookup"><span data-stu-id="c57ba-111">CN</span></span>                | <span data-ttu-id="c57ba-112">MS-IIS-FTP-dir</span><span class="sxs-lookup"><span data-stu-id="c57ba-112">ms-IIS-FTP-Dir</span></span>                                                                                                                  |
| <span data-ttu-id="c57ba-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c57ba-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c57ba-114">msIIS-FTPDir</span><span class="sxs-lookup"><span data-stu-id="c57ba-114">msIIS-FTPDir</span></span>                                                                                                                    |
| <span data-ttu-id="c57ba-115">Size</span><span class="sxs-lookup"><span data-stu-id="c57ba-115">Size</span></span>              | <span data-ttu-id="c57ba-116">30-50 Zeichen (15-25 Unicode-Zeichen für jede Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c57ba-116">30-50 characters (15-25 Unicode characters for each property)</span></span>                                                                   |
| <span data-ttu-id="c57ba-117">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c57ba-117">Update Privilege</span></span>  | <span data-ttu-id="c57ba-118">Domänen Administrator & lokales System</span><span class="sxs-lookup"><span data-stu-id="c57ba-118">Domain administrator & local system</span></span>                                                                                             |
| <span data-ttu-id="c57ba-119">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="c57ba-119">Update Frequency</span></span>  | <span data-ttu-id="c57ba-120">Diese Eigenschaft wird festgelegt, wenn der Administrator die Website erstellt und die FTP-Isolation festlegt.</span><span class="sxs-lookup"><span data-stu-id="c57ba-120">This property is set when the administrator creates the website and sets FTP isolation.</span></span> <span data-ttu-id="c57ba-121">Es wird nur selten geändert.</span><span class="sxs-lookup"><span data-stu-id="c57ba-121">It's rarely going to change after that.</span></span> |
| <span data-ttu-id="c57ba-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c57ba-122">Attribute-Id</span></span>      | <span data-ttu-id="c57ba-123">1.2.840.113556.1.4.1786</span><span class="sxs-lookup"><span data-stu-id="c57ba-123">1.2.840.113556.1.4.1786</span></span>                                                                                                         |
| <span data-ttu-id="c57ba-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c57ba-124">System-Id-Guid</span></span>    | <span data-ttu-id="c57ba-125">8a5c99e9-2230-46eb-b8e8-e59d712eb9ee</span><span class="sxs-lookup"><span data-stu-id="c57ba-125">8a5c99e9-2230-46eb-b8e8-e59d712eb9ee</span></span>                                                                                            |
| <span data-ttu-id="c57ba-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="c57ba-126">Syntax</span></span>            | [<span data-ttu-id="c57ba-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c57ba-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                     |



## <a name="implementations"></a><span data-ttu-id="c57ba-128">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="c57ba-128">Implementations</span></span>

-   [<span data-ttu-id="c57ba-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c57ba-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c57ba-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c57ba-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c57ba-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c57ba-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c57ba-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c57ba-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c57ba-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c57ba-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c57ba-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c57ba-134">Windows Server 2003</span></span>



| <span data-ttu-id="c57ba-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c57ba-135">Entry</span></span> | <span data-ttu-id="c57ba-136">Wert</span><span class="sxs-lookup"><span data-stu-id="c57ba-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c57ba-137">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c57ba-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c57ba-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c57ba-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c57ba-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="c57ba-139">System-Only</span></span>            | <span data-ttu-id="c57ba-140">False</span><span class="sxs-lookup"><span data-stu-id="c57ba-140">False</span></span>                             |
| <span data-ttu-id="c57ba-141">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c57ba-141">Is-Single-Valued</span></span>       | <span data-ttu-id="c57ba-142">Richtig</span><span class="sxs-lookup"><span data-stu-id="c57ba-142">True</span></span>                              |
| <span data-ttu-id="c57ba-143">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c57ba-143">Is Indexed</span></span>             | <span data-ttu-id="c57ba-144">False</span><span class="sxs-lookup"><span data-stu-id="c57ba-144">False</span></span>                             |
| <span data-ttu-id="c57ba-145">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c57ba-145">In Global Catalog</span></span>      | <span data-ttu-id="c57ba-146">False</span><span class="sxs-lookup"><span data-stu-id="c57ba-146">False</span></span>                             |
| <span data-ttu-id="c57ba-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c57ba-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="c57ba-148">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c57ba-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c57ba-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c57ba-149">Range-Lower</span></span>            | <span data-ttu-id="c57ba-150">1</span><span class="sxs-lookup"><span data-stu-id="c57ba-150">1</span></span>                                 |
| <span data-ttu-id="c57ba-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c57ba-151">Range-Upper</span></span>            | <span data-ttu-id="c57ba-152">256</span><span class="sxs-lookup"><span data-stu-id="c57ba-152">256</span></span>                               |
| <span data-ttu-id="c57ba-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c57ba-153">Search-Flags</span></span>           | <span data-ttu-id="c57ba-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c57ba-154">0x00000000</span></span>                        |
| <span data-ttu-id="c57ba-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c57ba-155">System-Flags</span></span>           | <span data-ttu-id="c57ba-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c57ba-156">0x00000010</span></span>                        |
| <span data-ttu-id="c57ba-157">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c57ba-157">Classes used in</span></span>        | [<span data-ttu-id="c57ba-158">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c57ba-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c57ba-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c57ba-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c57ba-160">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c57ba-160">Entry</span></span> | <span data-ttu-id="c57ba-161">Wert</span><span class="sxs-lookup"><span data-stu-id="c57ba-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c57ba-162">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c57ba-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c57ba-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c57ba-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c57ba-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="c57ba-164">System-Only</span></span>            | <span data-ttu-id="c57ba-165">False</span><span class="sxs-lookup"><span data-stu-id="c57ba-165">False</span></span>                             |
| <span data-ttu-id="c57ba-166">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c57ba-166">Is-Single-Valued</span></span>       | <span data-ttu-id="c57ba-167">Richtig</span><span class="sxs-lookup"><span data-stu-id="c57ba-167">True</span></span>                              |
| <span data-ttu-id="c57ba-168">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c57ba-168">Is Indexed</span></span>             | <span data-ttu-id="c57ba-169">False</span><span class="sxs-lookup"><span data-stu-id="c57ba-169">False</span></span>                             |
| <span data-ttu-id="c57ba-170">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c57ba-170">In Global Catalog</span></span>      | <span data-ttu-id="c57ba-171">False</span><span class="sxs-lookup"><span data-stu-id="c57ba-171">False</span></span>                             |
| <span data-ttu-id="c57ba-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c57ba-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="c57ba-173">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c57ba-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c57ba-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c57ba-174">Range-Lower</span></span>            | <span data-ttu-id="c57ba-175">1</span><span class="sxs-lookup"><span data-stu-id="c57ba-175">1</span></span>                                 |
| <span data-ttu-id="c57ba-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c57ba-176">Range-Upper</span></span>            | <span data-ttu-id="c57ba-177">256</span><span class="sxs-lookup"><span data-stu-id="c57ba-177">256</span></span>                               |
| <span data-ttu-id="c57ba-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c57ba-178">Search-Flags</span></span>           | <span data-ttu-id="c57ba-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c57ba-179">0x00000000</span></span>                        |
| <span data-ttu-id="c57ba-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c57ba-180">System-Flags</span></span>           | <span data-ttu-id="c57ba-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c57ba-181">0x00000010</span></span>                        |
| <span data-ttu-id="c57ba-182">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c57ba-182">Classes used in</span></span>        | [<span data-ttu-id="c57ba-183">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c57ba-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c57ba-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c57ba-184">Windows Server 2008</span></span>



| <span data-ttu-id="c57ba-185">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c57ba-185">Entry</span></span> | <span data-ttu-id="c57ba-186">Wert</span><span class="sxs-lookup"><span data-stu-id="c57ba-186">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c57ba-187">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c57ba-187">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c57ba-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c57ba-188">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c57ba-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="c57ba-189">System-Only</span></span>            | <span data-ttu-id="c57ba-190">False</span><span class="sxs-lookup"><span data-stu-id="c57ba-190">False</span></span>                             |
| <span data-ttu-id="c57ba-191">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c57ba-191">Is-Single-Valued</span></span>       | <span data-ttu-id="c57ba-192">Richtig</span><span class="sxs-lookup"><span data-stu-id="c57ba-192">True</span></span>                              |
| <span data-ttu-id="c57ba-193">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c57ba-193">Is Indexed</span></span>             | <span data-ttu-id="c57ba-194">False</span><span class="sxs-lookup"><span data-stu-id="c57ba-194">False</span></span>                             |
| <span data-ttu-id="c57ba-195">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c57ba-195">In Global Catalog</span></span>      | <span data-ttu-id="c57ba-196">False</span><span class="sxs-lookup"><span data-stu-id="c57ba-196">False</span></span>                             |
| <span data-ttu-id="c57ba-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c57ba-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="c57ba-198">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c57ba-198">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c57ba-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c57ba-199">Range-Lower</span></span>            | <span data-ttu-id="c57ba-200">1</span><span class="sxs-lookup"><span data-stu-id="c57ba-200">1</span></span>                                 |
| <span data-ttu-id="c57ba-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c57ba-201">Range-Upper</span></span>            | <span data-ttu-id="c57ba-202">256</span><span class="sxs-lookup"><span data-stu-id="c57ba-202">256</span></span>                               |
| <span data-ttu-id="c57ba-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c57ba-203">Search-Flags</span></span>           | <span data-ttu-id="c57ba-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c57ba-204">0x00000000</span></span>                        |
| <span data-ttu-id="c57ba-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c57ba-205">System-Flags</span></span>           | <span data-ttu-id="c57ba-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c57ba-206">0x00000010</span></span>                        |
| <span data-ttu-id="c57ba-207">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c57ba-207">Classes used in</span></span>        | [<span data-ttu-id="c57ba-208">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c57ba-208">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c57ba-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c57ba-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c57ba-210">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c57ba-210">Entry</span></span> | <span data-ttu-id="c57ba-211">Wert</span><span class="sxs-lookup"><span data-stu-id="c57ba-211">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c57ba-212">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c57ba-212">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c57ba-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c57ba-213">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c57ba-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="c57ba-214">System-Only</span></span>            | <span data-ttu-id="c57ba-215">False</span><span class="sxs-lookup"><span data-stu-id="c57ba-215">False</span></span>                             |
| <span data-ttu-id="c57ba-216">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c57ba-216">Is-Single-Valued</span></span>       | <span data-ttu-id="c57ba-217">Richtig</span><span class="sxs-lookup"><span data-stu-id="c57ba-217">True</span></span>                              |
| <span data-ttu-id="c57ba-218">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c57ba-218">Is Indexed</span></span>             | <span data-ttu-id="c57ba-219">False</span><span class="sxs-lookup"><span data-stu-id="c57ba-219">False</span></span>                             |
| <span data-ttu-id="c57ba-220">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c57ba-220">In Global Catalog</span></span>      | <span data-ttu-id="c57ba-221">False</span><span class="sxs-lookup"><span data-stu-id="c57ba-221">False</span></span>                             |
| <span data-ttu-id="c57ba-222">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c57ba-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="c57ba-223">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c57ba-223">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c57ba-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c57ba-224">Range-Lower</span></span>            | <span data-ttu-id="c57ba-225">1</span><span class="sxs-lookup"><span data-stu-id="c57ba-225">1</span></span>                                 |
| <span data-ttu-id="c57ba-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c57ba-226">Range-Upper</span></span>            | <span data-ttu-id="c57ba-227">256</span><span class="sxs-lookup"><span data-stu-id="c57ba-227">256</span></span>                               |
| <span data-ttu-id="c57ba-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c57ba-228">Search-Flags</span></span>           | <span data-ttu-id="c57ba-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c57ba-229">0x00000000</span></span>                        |
| <span data-ttu-id="c57ba-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c57ba-230">System-Flags</span></span>           | <span data-ttu-id="c57ba-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c57ba-231">0x00000010</span></span>                        |
| <span data-ttu-id="c57ba-232">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c57ba-232">Classes used in</span></span>        | [<span data-ttu-id="c57ba-233">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c57ba-233">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c57ba-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c57ba-234">Windows Server 2012</span></span>



| <span data-ttu-id="c57ba-235">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c57ba-235">Entry</span></span> | <span data-ttu-id="c57ba-236">Wert</span><span class="sxs-lookup"><span data-stu-id="c57ba-236">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c57ba-237">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c57ba-237">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c57ba-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c57ba-238">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c57ba-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="c57ba-239">System-Only</span></span>            | <span data-ttu-id="c57ba-240">False</span><span class="sxs-lookup"><span data-stu-id="c57ba-240">False</span></span>                             |
| <span data-ttu-id="c57ba-241">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c57ba-241">Is-Single-Valued</span></span>       | <span data-ttu-id="c57ba-242">Richtig</span><span class="sxs-lookup"><span data-stu-id="c57ba-242">True</span></span>                              |
| <span data-ttu-id="c57ba-243">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c57ba-243">Is Indexed</span></span>             | <span data-ttu-id="c57ba-244">False</span><span class="sxs-lookup"><span data-stu-id="c57ba-244">False</span></span>                             |
| <span data-ttu-id="c57ba-245">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c57ba-245">In Global Catalog</span></span>      | <span data-ttu-id="c57ba-246">False</span><span class="sxs-lookup"><span data-stu-id="c57ba-246">False</span></span>                             |
| <span data-ttu-id="c57ba-247">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c57ba-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="c57ba-248">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c57ba-248">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c57ba-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c57ba-249">Range-Lower</span></span>            | <span data-ttu-id="c57ba-250">1</span><span class="sxs-lookup"><span data-stu-id="c57ba-250">1</span></span>                                 |
| <span data-ttu-id="c57ba-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c57ba-251">Range-Upper</span></span>            | <span data-ttu-id="c57ba-252">256</span><span class="sxs-lookup"><span data-stu-id="c57ba-252">256</span></span>                               |
| <span data-ttu-id="c57ba-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c57ba-253">Search-Flags</span></span>           | <span data-ttu-id="c57ba-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c57ba-254">0x00000000</span></span>                        |
| <span data-ttu-id="c57ba-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c57ba-255">System-Flags</span></span>           | <span data-ttu-id="c57ba-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c57ba-256">0x00000010</span></span>                        |
| <span data-ttu-id="c57ba-257">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c57ba-257">Classes used in</span></span>        | [<span data-ttu-id="c57ba-258">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="c57ba-258">**User**</span></span>](c-user.md)<br/> |



 

 





