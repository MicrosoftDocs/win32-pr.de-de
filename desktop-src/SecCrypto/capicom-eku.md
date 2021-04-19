---
description: Definiert die Namen der erweiterten Schlüssel Verwendung, die darauf basieren, wo Sie verwendet werden können.
ms.assetid: 78f9f9cb-46e7-4f81-a16e-503750a0d743
title: CAPICOM_EKU-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EKU
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: e1d2f4f435fa31df00b87e20254aad57b690b047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359371"
---
# <a name="capicom_eku-enumeration"></a><span data-ttu-id="1eb17-103">CAPICOM- \_ EKU-Enumeration</span><span class="sxs-lookup"><span data-stu-id="1eb17-103">CAPICOM\_EKU enumeration</span></span>

<span data-ttu-id="1eb17-104">Der **CAPICOM- \_ EKU** -Enumerationstyp definiert die Namen der erweiterten Schlüssel Verwendung, die darauf basieren, wo Sie verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1eb17-104">The **CAPICOM\_EKU** enumeration type defines the extended key usage names based on where they can be used.</span></span>

## <a name="members"></a><span data-ttu-id="1eb17-105">Member</span><span class="sxs-lookup"><span data-stu-id="1eb17-105">Members</span></span>



| <span data-ttu-id="1eb17-106">Member</span><span class="sxs-lookup"><span data-stu-id="1eb17-106">Member</span></span>                                     | <span data-ttu-id="1eb17-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1eb17-107">Description</span></span>                                                                                                                                                 | <span data-ttu-id="1eb17-108">Wert</span><span class="sxs-lookup"><span data-stu-id="1eb17-108">Value</span></span> |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="1eb17-109">**Weitere CAPICOM- \_ EKU \_ other**</span><span class="sxs-lookup"><span data-stu-id="1eb17-109">**CAPICOM\_EKU\_OTHER**</span></span>                    | <span data-ttu-id="1eb17-110">Das Zertifikat verfügt über in der lokalen Richtlinie definierte Verwendung.</span><span class="sxs-lookup"><span data-stu-id="1eb17-110">Certificate has uses defined in local policy.</span></span> <span data-ttu-id="1eb17-111">Diese wird verwendet, wenn die erforderliche EKU nicht vordefiniert ist und der OID-Wert von der Anwendung festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="1eb17-111">This is used if the EKU needed is not predefined and the OID value must be set by the application.</span></span><br/> | <span data-ttu-id="1eb17-112">0</span><span class="sxs-lookup"><span data-stu-id="1eb17-112">0</span></span>     |
| <span data-ttu-id="1eb17-113">**CAPICOM- \_ EKU- \_ Server Authentifizierung \_**</span><span class="sxs-lookup"><span data-stu-id="1eb17-113">**CAPICOM\_EKU\_SERVER\_AUTH**</span></span>             | <span data-ttu-id="1eb17-114">Das Zertifikat kann zum Authentifizieren eines Servers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1eb17-114">Certificate can be used to authenticate a server.</span></span><br/>                                                                                                | <span data-ttu-id="1eb17-115">1</span><span class="sxs-lookup"><span data-stu-id="1eb17-115">1</span></span>     |
| <span data-ttu-id="1eb17-116">**CAPICOM- \_ EKU- \_ Client Authentifizierung \_**</span><span class="sxs-lookup"><span data-stu-id="1eb17-116">**CAPICOM\_EKU\_CLIENT\_AUTH**</span></span>             | <span data-ttu-id="1eb17-117">Das Zertifikat kann zum Authentifizieren eines Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1eb17-117">Certificate can be used to authenticate a client.</span></span><br/>                                                                                                | <span data-ttu-id="1eb17-118">2</span><span class="sxs-lookup"><span data-stu-id="1eb17-118">2</span></span>     |
| <span data-ttu-id="1eb17-119">**CAPICOM- \_ EKU- \_ Code \_ Signatur**</span><span class="sxs-lookup"><span data-stu-id="1eb17-119">**CAPICOM\_EKU\_CODE\_SIGNING**</span></span>            | <span data-ttu-id="1eb17-120">Das Zertifikat kann verwendet werden, um eine digitale Signatur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1eb17-120">Certificate can be used to create a digital signature.</span></span><br/>                                                                                           | <span data-ttu-id="1eb17-121">3</span><span class="sxs-lookup"><span data-stu-id="1eb17-121">3</span></span>     |
| <span data-ttu-id="1eb17-122">**CAPICOM \_ EKU \_ -e-Mail- \_ Schutz**</span><span class="sxs-lookup"><span data-stu-id="1eb17-122">**CAPICOM\_EKU\_EMAIL\_PROTECTION**</span></span>        | <span data-ttu-id="1eb17-123">Zertifikat kann für den e-Mail-Schutz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1eb17-123">Certificate can be used for email protection.</span></span><br/>                                                                                                    | <span data-ttu-id="1eb17-124">4</span><span class="sxs-lookup"><span data-stu-id="1eb17-124">4</span></span>     |
| <span data-ttu-id="1eb17-125">**CAPICOM \_ EKU \_ Smartcard- \_ Anmeldung**</span><span class="sxs-lookup"><span data-stu-id="1eb17-125">**CAPICOM\_EKU\_SMARTCARD\_LOGON**</span></span>         | <span data-ttu-id="1eb17-126">Das Zertifikat kann für die Smartcard-Anmeldung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1eb17-126">Certificate can be used for smart card logon.</span></span> <span data-ttu-id="1eb17-127">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="1eb17-127">Introduced in CAPICOM 2.0.</span></span><br/>                                                                         | <span data-ttu-id="1eb17-128">5</span><span class="sxs-lookup"><span data-stu-id="1eb17-128">5</span></span>     |
| <span data-ttu-id="1eb17-129">**CAPICOM- \_ EKU- \_ verschlüsselndes \_ Datei \_ System**</span><span class="sxs-lookup"><span data-stu-id="1eb17-129">**CAPICOM\_EKU\_ENCRYPTING\_FILE\_SYSTEM**</span></span> | <span data-ttu-id="1eb17-130">Das Zertifikat kann für EFS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1eb17-130">Certificate can be used for EFS.</span></span> <span data-ttu-id="1eb17-131">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="1eb17-131">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                      | <span data-ttu-id="1eb17-132">6</span><span class="sxs-lookup"><span data-stu-id="1eb17-132">6</span></span>     |



## <a name="remarks"></a><span data-ttu-id="1eb17-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1eb17-133">Remarks</span></span>

<span data-ttu-id="1eb17-134">Der **\_ EKU** -Enumerationstyp CAPICOM wird von der [**EKU verwendet. Name**](eku-name.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1eb17-134">The **CAPICOM\_EKU** enumeration type is used by the [**EKU.Name**](eku-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eb17-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1eb17-135">Requirements</span></span>



| <span data-ttu-id="1eb17-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1eb17-136">Requirement</span></span> | <span data-ttu-id="1eb17-137">Wert</span><span class="sxs-lookup"><span data-stu-id="1eb17-137">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb17-138">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="1eb17-138">Redistributable</span></span><br/> | <span data-ttu-id="1eb17-139">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="1eb17-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="1eb17-140">Header</span><span class="sxs-lookup"><span data-stu-id="1eb17-140">Header</span></span><br/>          | <dl> <span data-ttu-id="1eb17-141"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="1eb17-141"><dt>Capicom.h</dt></span></span> </dl> |



 

 




