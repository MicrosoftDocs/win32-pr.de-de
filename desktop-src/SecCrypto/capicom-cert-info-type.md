---
description: Definiert, welche Informationen von einem Zertifikat abgefragt werden sollen.
ms.assetid: b603c06b-e6d4-4d5d-92b2-3b4f5b93478a
title: CAPICOM_CERT_INFO_TYPE-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERT_INFO_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 8e38bb8940645bbefecb3822bce8de8c2e0eb902
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360418"
---
# <a name="capicom_cert_info_type-enumeration"></a><span data-ttu-id="e7b5a-103">CAPICOM \_ CERT \_ - \_ Infotyp-Enumeration</span><span class="sxs-lookup"><span data-stu-id="e7b5a-103">CAPICOM\_CERT\_INFO\_TYPE enumeration</span></span>

<span data-ttu-id="e7b5a-104">Der Typ " **CAPICOM \_ CERT \_ Info \_ Type** Enumeration" definiert, welche Informationen von einem Zertifikat abgefragt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e7b5a-104">The **CAPICOM\_CERT\_INFO\_TYPE** enumeration type defines what information is to be queried from a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="e7b5a-105">Member</span><span class="sxs-lookup"><span data-stu-id="e7b5a-105">Members</span></span>



| <span data-ttu-id="e7b5a-106">Member</span><span class="sxs-lookup"><span data-stu-id="e7b5a-106">Member</span></span>                                         | <span data-ttu-id="e7b5a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7b5a-107">Description</span></span>                                                                                  | <span data-ttu-id="e7b5a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="e7b5a-108">Value</span></span> |
|------------------------------------------------|----------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="e7b5a-109">**CAPICOM \_ CERT \_ Info \_ Subject \_ Simple \_ Name**</span><span class="sxs-lookup"><span data-stu-id="e7b5a-109">**CAPICOM\_CERT\_INFO\_SUBJECT\_SIMPLE\_NAME**</span></span> | <span data-ttu-id="e7b5a-110">Gibt den anzeigen amen des Zertifikats Antragstellers zurück.</span><span class="sxs-lookup"><span data-stu-id="e7b5a-110">Returns the display name of the certificate subject.</span></span><br/>                              | <span data-ttu-id="e7b5a-111">0</span><span class="sxs-lookup"><span data-stu-id="e7b5a-111">0</span></span>     |
| <span data-ttu-id="e7b5a-112">**Name der von CAPICOM \_ CERT \_ Info \_ Aussteller \_ einfacher \_**</span><span class="sxs-lookup"><span data-stu-id="e7b5a-112">**CAPICOM\_CERT\_INFO\_ISSUER\_SIMPLE\_NAME**</span></span>  | <span data-ttu-id="e7b5a-113">Gibt den anzeigen amen des Zertifikats Ausstellers zurück.</span><span class="sxs-lookup"><span data-stu-id="e7b5a-113">Returns the display name of the issuer of the certificate.</span></span><br/>                        | <span data-ttu-id="e7b5a-114">1</span><span class="sxs-lookup"><span data-stu-id="e7b5a-114">1</span></span>     |
| <span data-ttu-id="e7b5a-115">**Name der "CAPICOM \_ CERT \_ Info \_ Subject \_ Email \_ "**</span><span class="sxs-lookup"><span data-stu-id="e7b5a-115">**CAPICOM\_CERT\_INFO\_SUBJECT\_EMAIL\_NAME**</span></span>  | <span data-ttu-id="e7b5a-116">Gibt die e-Mail-Adresse des Zertifikat Antragstellers zurück.</span><span class="sxs-lookup"><span data-stu-id="e7b5a-116">Returns the email address of the certificate subject.</span></span><br/>                             | <span data-ttu-id="e7b5a-117">2</span><span class="sxs-lookup"><span data-stu-id="e7b5a-117">2</span></span>     |
| <span data-ttu-id="e7b5a-118">**Name der \_ \_ \_ Aussteller \_ -e-Mail \_ des CAPICOM-Zertifikats**</span><span class="sxs-lookup"><span data-stu-id="e7b5a-118">**CAPICOM\_CERT\_INFO\_ISSUER\_EMAIL\_NAME**</span></span>   | <span data-ttu-id="e7b5a-119">Gibt die e-Mail-Adresse des Zertifikats Ausstellers zurück.</span><span class="sxs-lookup"><span data-stu-id="e7b5a-119">Returns the email address of the issuer of the certificate.</span></span><br/>                       | <span data-ttu-id="e7b5a-120">3</span><span class="sxs-lookup"><span data-stu-id="e7b5a-120">3</span></span>     |
| <span data-ttu-id="e7b5a-121">**Antragsteller \_ - \_ \_ \_ UPN für CAPICOM CERT Info**</span><span class="sxs-lookup"><span data-stu-id="e7b5a-121">**CAPICOM\_CERT\_INFO\_SUBJECT\_UPN**</span></span>          | <span data-ttu-id="e7b5a-122">Gibt den UPN des Zertifikat Antragstellers zurück.</span><span class="sxs-lookup"><span data-stu-id="e7b5a-122">Returns the UPN of the certificate subject.</span></span> <span data-ttu-id="e7b5a-123">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="e7b5a-123">Introduced in CAPICOM 2.0.</span></span><br/>            | <span data-ttu-id="e7b5a-124">4</span><span class="sxs-lookup"><span data-stu-id="e7b5a-124">4</span></span>     |
| <span data-ttu-id="e7b5a-125">**-UPN des CAPICOM \_ CERT \_ Info- \_ Ausstellers \_**</span><span class="sxs-lookup"><span data-stu-id="e7b5a-125">**CAPICOM\_CERT\_INFO\_ISSUER\_UPN**</span></span>           | <span data-ttu-id="e7b5a-126">Gibt den UPN des Zertifikats Ausstellers zurück.</span><span class="sxs-lookup"><span data-stu-id="e7b5a-126">Returns the UPN of the issuer of the certificate.</span></span> <span data-ttu-id="e7b5a-127">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="e7b5a-127">Introduced in CAPICOM 2.0.</span></span><br/>      | <span data-ttu-id="e7b5a-128">5</span><span class="sxs-lookup"><span data-stu-id="e7b5a-128">5</span></span>     |
| <span data-ttu-id="e7b5a-129">**"CAPICOM \_ CERT \_ Info \_ Subject \_ DNS \_ Name"**</span><span class="sxs-lookup"><span data-stu-id="e7b5a-129">**CAPICOM\_CERT\_INFO\_SUBJECT\_DNS\_NAME**</span></span>    | <span data-ttu-id="e7b5a-130">Gibt den DNS-Namen des Zertifikat Antragstellers zurück.</span><span class="sxs-lookup"><span data-stu-id="e7b5a-130">Returns the DNS name of the certificate subject.</span></span> <span data-ttu-id="e7b5a-131">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="e7b5a-131">Introduced in CAPICOM 2.0.</span></span><br/>       | <span data-ttu-id="e7b5a-132">6</span><span class="sxs-lookup"><span data-stu-id="e7b5a-132">6</span></span>     |
| <span data-ttu-id="e7b5a-133">**Name des CAPICOM \_ CERT \_ Info-Aussteller- \_ \_ DNS \_**</span><span class="sxs-lookup"><span data-stu-id="e7b5a-133">**CAPICOM\_CERT\_INFO\_ISSUER\_DNS\_NAME**</span></span>     | <span data-ttu-id="e7b5a-134">Gibt den DNS-Namen des Zertifikats Ausstellers zurück.</span><span class="sxs-lookup"><span data-stu-id="e7b5a-134">Returns the DNS name of the issuer of the certificate.</span></span> <span data-ttu-id="e7b5a-135">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="e7b5a-135">Introduced in CAPICOM 2.0.</span></span><br/> | <span data-ttu-id="e7b5a-136">7</span><span class="sxs-lookup"><span data-stu-id="e7b5a-136">7</span></span>     |



## <a name="remarks"></a><span data-ttu-id="e7b5a-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7b5a-137">Remarks</span></span>

<span data-ttu-id="e7b5a-138">Der-Enumerationstyp des **CAPICOM- \_ CERT- \_ \_ Typs** wird von der [**Certificate. GetInfo**](certificate-getinfo.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7b5a-138">The **CAPICOM\_CERT\_INFO\_TYPE** enumeration type is used by the [**Certificate.GetInfo**](certificate-getinfo.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b5a-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7b5a-139">Requirements</span></span>



| <span data-ttu-id="e7b5a-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7b5a-140">Requirement</span></span> | <span data-ttu-id="e7b5a-141">Wert</span><span class="sxs-lookup"><span data-stu-id="e7b5a-141">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b5a-142">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e7b5a-142">Redistributable</span></span><br/> | <span data-ttu-id="e7b5a-143">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="e7b5a-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="e7b5a-144">Header</span><span class="sxs-lookup"><span data-stu-id="e7b5a-144">Header</span></span><br/>          | <dl> <span data-ttu-id="e7b5a-145"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7b5a-145"><dt>Capicom.h</dt></span></span> </dl> |



 

 




