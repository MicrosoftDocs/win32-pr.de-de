---
description: Der-Enumerationstyp "CAPICOM \_ Certificate \_ Find \_ Type" definiert den Typ der Suchkriterien, die zum Suchen nach bestimmten Zertifikaten verwendet werden. Dieser Enumerationstyp wurde in CAPICOM 2,0 eingeführt.
ms.assetid: d71436e5-d921-4b84-8028-301d8fc4aedb
title: CAPICOM_CERTIFICATE_FIND_TYPE-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_FIND_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: c5c867b230ba2045d97619d7f55e257bd7803b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358253"
---
# <a name="capicom_certificate_find_type-enumeration"></a><span data-ttu-id="7c4a3-104">CAPICOM \_ - \_ \_ Zertifikattyp-Enumeration</span><span class="sxs-lookup"><span data-stu-id="7c4a3-104">CAPICOM\_CERTIFICATE\_FIND\_TYPE enumeration</span></span>

<span data-ttu-id="7c4a3-105">Der-Enumerationstyp " **CAPICOM \_ Certificate \_ Find \_ Type** " definiert den Typ der Suchkriterien, die zum Suchen nach bestimmten Zertifikaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-105">The **CAPICOM\_CERTIFICATE\_FIND\_TYPE** enumeration type defines the type of search criteria used to find specific certificates.</span></span> <span data-ttu-id="7c4a3-106">Dieser Enumerationstyp wurde in CAPICOM 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-106">This enumeration type was introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="7c4a3-107">Member</span><span class="sxs-lookup"><span data-stu-id="7c4a3-107">Members</span></span>



| <span data-ttu-id="7c4a3-108">Member</span><span class="sxs-lookup"><span data-stu-id="7c4a3-108">Member</span></span>                                                | <span data-ttu-id="7c4a3-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c4a3-109">Description</span></span>                                                                                                                                 | <span data-ttu-id="7c4a3-110">Wert</span><span class="sxs-lookup"><span data-stu-id="7c4a3-110">Value</span></span> |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="7c4a3-111">**CAPICOM- \_ Zertifikat \_ Suche SHA1- \_ \_ Hash**</span><span class="sxs-lookup"><span data-stu-id="7c4a3-111">**CAPICOM\_CERTIFICATE\_FIND\_SHA1\_HASH**</span></span>            | <span data-ttu-id="7c4a3-112">Gibt Zertifikate zurück, die einem angegebenen SHA1-Hash entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-112">Returns certificates matching a specified SHA1 hash.</span></span><br/>                                                                             | <span data-ttu-id="7c4a3-113">0</span><span class="sxs-lookup"><span data-stu-id="7c4a3-113">0</span></span>     |
| <span data-ttu-id="7c4a3-114">**CAPICOM-Zertifikat suchantrags Teller \_ \_ \_ \_ Name**</span><span class="sxs-lookup"><span data-stu-id="7c4a3-114">**CAPICOM\_CERTIFICATE\_FIND\_SUBJECT\_NAME**</span></span>         | <span data-ttu-id="7c4a3-115">Gibt Zertifikate zurück, deren Antragsteller Name dem angegebenen Antragsteller Namen genau oder teilweise entspricht.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-115">Returns certificates whose subject name exactly or partially matches a specified subject name.</span></span><br/>                                   | <span data-ttu-id="7c4a3-116">1</span><span class="sxs-lookup"><span data-stu-id="7c4a3-116">1</span></span>     |
| <span data-ttu-id="7c4a3-117">**CAPICOM- \_ Zertifikat \_ Suchen des \_ Aussteller \_ namens**</span><span class="sxs-lookup"><span data-stu-id="7c4a3-117">**CAPICOM\_CERTIFICATE\_FIND\_ISSUER\_NAME**</span></span>          | <span data-ttu-id="7c4a3-118">Gibt Zertifikate zurück, deren Aussteller Name exakt oder teilweise mit einem angegebenen Aussteller Namen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-118">Returns certificates whose issuer name exactly or partially matches a specified issuer name.</span></span><br/>                                     | <span data-ttu-id="7c4a3-119">2</span><span class="sxs-lookup"><span data-stu-id="7c4a3-119">2</span></span>     |
| <span data-ttu-id="7c4a3-120">**CAPICOM- \_ Zertifikat \_ \_ \_ suchstammname**</span><span class="sxs-lookup"><span data-stu-id="7c4a3-120">**CAPICOM\_CERTIFICATE\_FIND\_ROOT\_NAME**</span></span>            | <span data-ttu-id="7c4a3-121">Gibt Zertifikate zurück, deren Stamm Antragsteller Name exakt oder teilweise mit einem angegebenen Stamm Antragsteller Namen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-121">Returns certificates whose root subject name exactly or partially matches a specified root subject name.</span></span><br/>                         | <span data-ttu-id="7c4a3-122">3</span><span class="sxs-lookup"><span data-stu-id="7c4a3-122">3</span></span>     |
| <span data-ttu-id="7c4a3-123">**CAPICOM- \_ Zertifikat \_ Suchen \_ Vorlagen \_ Name**</span><span class="sxs-lookup"><span data-stu-id="7c4a3-123">**CAPICOM\_CERTIFICATE\_FIND\_TEMPLATE\_NAME**</span></span>        | <span data-ttu-id="7c4a3-124">Gibt Zertifikate zurück, deren Vorlagen Name mit einem angegebenen Vorlagen Namen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-124">Returns certificates whose template name matches a specified template name.</span></span><br/>                                                      | <span data-ttu-id="7c4a3-125">4</span><span class="sxs-lookup"><span data-stu-id="7c4a3-125">4</span></span>     |
| <span data-ttu-id="7c4a3-126">**CAPICOM- \_ Zertifikat \_ Suche- \_ Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="7c4a3-126">**CAPICOM\_CERTIFICATE\_FIND\_EXTENSION**</span></span>             | <span data-ttu-id="7c4a3-127">Gibt Zertifikate zurück, die eine Erweiterung aufweisen, die mit einer angegebenen Erweiterung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-127">Returns certificates that have an extension that matches a specified extension.</span></span><br/>                                                  | <span data-ttu-id="7c4a3-128">5</span><span class="sxs-lookup"><span data-stu-id="7c4a3-128">5</span></span>     |
| <span data-ttu-id="7c4a3-129">**CAPICOM- \_ Zertifikat für \_ \_ Erweiterte \_ Eigenschaft suchen**</span><span class="sxs-lookup"><span data-stu-id="7c4a3-129">**CAPICOM\_CERTIFICATE\_FIND\_EXTENDED\_PROPERTY**</span></span>    | <span data-ttu-id="7c4a3-130">Gibt Zertifikate mit einer erweiterten Eigenschaft zurück, deren Eigenschaften Bezeichner mit einem angegebenen Eigenschaften Bezeichner übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-130">Returns certificates that have an extended property whose property identifier matches a specified property identifier.</span></span><br/>           | <span data-ttu-id="7c4a3-131">6</span><span class="sxs-lookup"><span data-stu-id="7c4a3-131">6</span></span>     |
| <span data-ttu-id="7c4a3-132">**CAPICOM- \_ Zertifikat \_ Suche- \_ Anwendungs \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="7c4a3-132">**CAPICOM\_CERTIFICATE\_FIND\_APPLICATION\_POLICY**</span></span>   | <span data-ttu-id="7c4a3-133">Gibt Zertifikate im Speicher zurück, die entweder über eine erweiterte Schlüssel Verwendungs Erweiterung oder-Eigenschaft in Kombination mit einem Verwendungs Bezeichner verfügen.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-133">Returns certificates in the store that have either an enhanced key usage extension or property combined with a usage identifier.</span></span><br/> | <span data-ttu-id="7c4a3-134">7</span><span class="sxs-lookup"><span data-stu-id="7c4a3-134">7</span></span>     |
| <span data-ttu-id="7c4a3-135">**CAPICOM- \_ Zertifikat Zertifikat \_ \_ \_ Richtlinie suchen**</span><span class="sxs-lookup"><span data-stu-id="7c4a3-135">**CAPICOM\_CERTIFICATE\_FIND\_CERTIFICATE\_POLICY**</span></span>   | <span data-ttu-id="7c4a3-136">Gibt Zertifikate zurück, die eine angegebene Richtlinien OID enthalten.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-136">Returns certificates containing a specified policy OID.</span></span><br/>                                                                          | <span data-ttu-id="7c4a3-137">8</span><span class="sxs-lookup"><span data-stu-id="7c4a3-137">8</span></span>     |
| <span data-ttu-id="7c4a3-138">**zulässige Zeit für CAPICOM- \_ Zertifikat \_ Suche \_ \_ gültig**</span><span class="sxs-lookup"><span data-stu-id="7c4a3-138">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_VALID**</span></span>           | <span data-ttu-id="7c4a3-139">Gibt Zertifikate zurück, deren Zeit gültig ist.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-139">Returns certificates whose time is valid.</span></span><br/>                                                                                        | <span data-ttu-id="7c4a3-140">9</span><span class="sxs-lookup"><span data-stu-id="7c4a3-140">9</span></span>     |
| <span data-ttu-id="7c4a3-141">**Das CAPICOM- \_ Zertifikat ist \_ \_ \_ \_ noch nicht \_ gültig.**</span><span class="sxs-lookup"><span data-stu-id="7c4a3-141">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_NOT\_YET\_VALID**</span></span> | <span data-ttu-id="7c4a3-142">Gibt Zertifikate zurück, deren Zeit noch nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-142">Returns certificates whose time is not yet valid.</span></span><br/>                                                                                | <span data-ttu-id="7c4a3-143">10</span><span class="sxs-lookup"><span data-stu-id="7c4a3-143">10</span></span>    |
| <span data-ttu-id="7c4a3-144">**Zeit für das CAPICOM- \_ Zertifikat ist \_ \_ \_ abgelaufen.**</span><span class="sxs-lookup"><span data-stu-id="7c4a3-144">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_EXPIRED**</span></span>         | <span data-ttu-id="7c4a3-145">Gibt Zertifikate zurück, deren Zeit abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-145">Returns certificates whose time has expired.</span></span><br/>                                                                                     | <span data-ttu-id="7c4a3-146">11</span><span class="sxs-lookup"><span data-stu-id="7c4a3-146">11</span></span>    |
| <span data-ttu-id="7c4a3-147">**CAPICOM- \_ Zertifikat \_ Suche \_ Schlüssel \_ Verwendung**</span><span class="sxs-lookup"><span data-stu-id="7c4a3-147">**CAPICOM\_CERTIFICATE\_FIND\_KEY\_USAGE**</span></span>            | <span data-ttu-id="7c4a3-148">Gibt Zertifikate zurück, die einen Schlüssel enthalten, der in der angegebenen Weise verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-148">Returns certificates containing a key that can be used in the specified manner.</span></span><br/>                                                  | <span data-ttu-id="7c4a3-149">12</span><span class="sxs-lookup"><span data-stu-id="7c4a3-149">12</span></span>    |



## <a name="remarks"></a><span data-ttu-id="7c4a3-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c4a3-150">Remarks</span></span>

<span data-ttu-id="7c4a3-151">Der-Enumerationstyp " **CAPICOM \_ Certificate \_ Find \_ Type** " wird von der Certificate [**. Find**](certificates-find.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-151">The **CAPICOM\_CERTIFICATE\_FIND\_TYPE** enumeration type is used by the [**Certificates.Find**](certificates-find.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c4a3-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c4a3-152">Requirements</span></span>



| <span data-ttu-id="7c4a3-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c4a3-153">Requirement</span></span> | <span data-ttu-id="7c4a3-154">Wert</span><span class="sxs-lookup"><span data-stu-id="7c4a3-154">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7c4a3-155">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="7c4a3-155">Redistributable</span></span><br/> | <span data-ttu-id="7c4a3-156">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="7c4a3-156">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="7c4a3-157">Header</span><span class="sxs-lookup"><span data-stu-id="7c4a3-157">Header</span></span><br/>          | <dl> <span data-ttu-id="7c4a3-158"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c4a3-158"><dt>Capicom.h</dt></span></span> </dl> |



 

 




