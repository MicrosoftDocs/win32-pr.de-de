---
title: MS-DNS-NSEC3-User-Salt-Attribut
description: Ein Attribut, das eine vom Benutzer angegebene NSEC3 Salt-Zeichenfolge definiert, die beim Signieren der DNS-Zone verwendet werden soll. Wenn leer, wird zufälliger Salt verwendet.
ms.assetid: b9829732-8a79-4f07-8644-9fe4ba05ba8f
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-DNS-NSEC3-User-Salt-Attribut
- MSDNs-NSEC3UserSalt-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-DNS-NSEC3-User-Salt
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d28acb28dec95ef13afc37f9d7f26d713d5cf9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744753"
---
# <a name="ms-dns-nsec3-user-salt-attribute"></a><span data-ttu-id="c9b5d-106">MS-DNS-NSEC3-User-Salt-Attribut</span><span class="sxs-lookup"><span data-stu-id="c9b5d-106">ms-DNS-NSEC3-User-Salt attribute</span></span>

<span data-ttu-id="c9b5d-107">Ein Attribut, das eine vom Benutzer angegebene NSEC3 Salt-Zeichenfolge definiert, die beim Signieren der DNS-Zone verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9b5d-107">An attribute that defines a user-specified NSEC3 salt string to use when signing the DNS zone.</span></span> <span data-ttu-id="c9b5d-108">Wenn leer, wird zufälliger Salt verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9b5d-108">If empty, random salt will be used.</span></span>



| <span data-ttu-id="c9b5d-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c9b5d-109">Entry</span></span> | <span data-ttu-id="c9b5d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="c9b5d-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c9b5d-111">CN</span><span class="sxs-lookup"><span data-stu-id="c9b5d-111">CN</span></span>                | <span data-ttu-id="c9b5d-112">MS-DNS-NSEC3-User-Salt</span><span class="sxs-lookup"><span data-stu-id="c9b5d-112">ms-DNS-NSEC3-User-Salt</span></span>                      |
| <span data-ttu-id="c9b5d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c9b5d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c9b5d-114">MSDNs-NSEC3UserSalt</span><span class="sxs-lookup"><span data-stu-id="c9b5d-114">msDNS-NSEC3UserSalt</span></span>                         |
| <span data-ttu-id="c9b5d-115">Size</span><span class="sxs-lookup"><span data-stu-id="c9b5d-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="c9b5d-116">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c9b5d-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="c9b5d-117">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="c9b5d-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="c9b5d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c9b5d-118">Attribute-Id</span></span>      | <span data-ttu-id="c9b5d-119">1.2.840.113556.1.4.2148</span><span class="sxs-lookup"><span data-stu-id="c9b5d-119">1.2.840.113556.1.4.2148</span></span>                     |
| <span data-ttu-id="c9b5d-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c9b5d-120">System-Id-Guid</span></span>    | <span data-ttu-id="c9b5d-121">aff16770-9622-4fbc-a128-3088777605b9</span><span class="sxs-lookup"><span data-stu-id="c9b5d-121">aff16770-9622-4fbc-a128-3088777605b9</span></span>        |
| <span data-ttu-id="c9b5d-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9b5d-122">Syntax</span></span>            | [<span data-ttu-id="c9b5d-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c9b5d-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c9b5d-124">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="c9b5d-124">Implementations</span></span>

-   [<span data-ttu-id="c9b5d-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c9b5d-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="c9b5d-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9b5d-126">Windows Server 2012</span></span>



| <span data-ttu-id="c9b5d-127">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c9b5d-127">Entry</span></span> | <span data-ttu-id="c9b5d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c9b5d-128">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c9b5d-129">Link-ID</span><span class="sxs-lookup"><span data-stu-id="c9b5d-129">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c9b5d-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c9b5d-130">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c9b5d-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="c9b5d-131">System-Only</span></span>            | <span data-ttu-id="c9b5d-132">False</span><span class="sxs-lookup"><span data-stu-id="c9b5d-132">False</span></span>                                    |
| <span data-ttu-id="c9b5d-133">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="c9b5d-133">Is-Single-Valued</span></span>       | <span data-ttu-id="c9b5d-134">Richtig</span><span class="sxs-lookup"><span data-stu-id="c9b5d-134">True</span></span>                                     |
| <span data-ttu-id="c9b5d-135">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="c9b5d-135">Is Indexed</span></span>             | <span data-ttu-id="c9b5d-136">False</span><span class="sxs-lookup"><span data-stu-id="c9b5d-136">False</span></span>                                    |
| <span data-ttu-id="c9b5d-137">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="c9b5d-137">In Global Catalog</span></span>      | <span data-ttu-id="c9b5d-138">False</span><span class="sxs-lookup"><span data-stu-id="c9b5d-138">False</span></span>                                    |
| <span data-ttu-id="c9b5d-139">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c9b5d-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="c9b5d-140">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="c9b5d-140">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c9b5d-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c9b5d-141">Range-Lower</span></span>            | <span data-ttu-id="c9b5d-142">0</span><span class="sxs-lookup"><span data-stu-id="c9b5d-142">0</span></span>                                        |
| <span data-ttu-id="c9b5d-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c9b5d-143">Range-Upper</span></span>            | <span data-ttu-id="c9b5d-144">510</span><span class="sxs-lookup"><span data-stu-id="c9b5d-144">510</span></span>                                      |
| <span data-ttu-id="c9b5d-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c9b5d-145">Search-Flags</span></span>           | <span data-ttu-id="c9b5d-146">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c9b5d-146">0x00000008</span></span>                               |
| <span data-ttu-id="c9b5d-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c9b5d-147">System-Flags</span></span>           | <span data-ttu-id="c9b5d-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c9b5d-148">0x00000010</span></span>                               |
| <span data-ttu-id="c9b5d-149">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="c9b5d-149">Classes used in</span></span>        | [<span data-ttu-id="c9b5d-150">**DNS-Zone**</span><span class="sxs-lookup"><span data-stu-id="c9b5d-150">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 





