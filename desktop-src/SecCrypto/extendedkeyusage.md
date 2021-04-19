---
description: Bietet schreibgeschützten Zugriff auf die Eigenschaften der erweiterten Schlüssel Verwendung (Extended Key Usage, EKU) eines Zertifikats.
ms.assetid: 636d7f65-d286-4800-a576-a23e6e9811b2
title: Extendedkeyusage-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a93be1f6fe75559d0284ca955ca5b6e9c516eed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367690"
---
# <a name="extendedkeyusage-object"></a><span data-ttu-id="5f69f-103">Extendedkeyusage-Objekt</span><span class="sxs-lookup"><span data-stu-id="5f69f-103">ExtendedKeyUsage object</span></span>

<span data-ttu-id="5f69f-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5f69f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="5f69f-105">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="5f69f-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="5f69f-106">Das **extendedkeyusage** -Objekt bietet schreibgeschützten Zugriff auf die Eigenschaften der erweiterten Schlüssel Verwendung (Extended Key Usage, EKU) eines Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="5f69f-106">The **ExtendedKeyUsage** object provides read-only access to the extended key usage (EKU) properties of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="5f69f-107">Member</span><span class="sxs-lookup"><span data-stu-id="5f69f-107">Members</span></span>

<span data-ttu-id="5f69f-108">Das **extendedkeyusage** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5f69f-108">The **ExtendedKeyUsage** object has these types of members:</span></span>

-   [<span data-ttu-id="5f69f-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f69f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f69f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f69f-110">Properties</span></span>

<span data-ttu-id="5f69f-111">Das **extendedkeyusage** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5f69f-111">The **ExtendedKeyUsage** object has these properties.</span></span>



| <span data-ttu-id="5f69f-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5f69f-112">Property</span></span>                                                     | <span data-ttu-id="5f69f-113">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="5f69f-113">Access type</span></span>          | <span data-ttu-id="5f69f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f69f-114">Description</span></span>                                                                                                                             |
|:-------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f69f-115">**EKUs**</span><span class="sxs-lookup"><span data-stu-id="5f69f-115">**EKUs**</span></span>](extendedkeyusage-ekus.md)<br/>             | <span data-ttu-id="5f69f-116">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f69f-116">Read-only</span></span><br/> | <span data-ttu-id="5f69f-117">[**EKUs**](ekus.md) -Sammlung, die die [**EKU**](eku.md) -Objekte für das Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="5f69f-117">[**EKUs**](ekus.md) collection that contains the [**EKU**](eku.md) objects for the certificate.</span></span><br/>                            |
| [<span data-ttu-id="5f69f-118">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="5f69f-118">**IsCritical**</span></span>](extendedkeyusage-iscritical.md)<br/> | <span data-ttu-id="5f69f-119">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f69f-119">Read-only</span></span><br/> | <span data-ttu-id="5f69f-120">Ruft einen **booleschen** Wert ab, der angibt, ob die EKU-Erweiterung als kritisch markiert ist.</span><span class="sxs-lookup"><span data-stu-id="5f69f-120">Retrieves a **Boolean** value that indicates whether the EKU extension is marked critical.</span></span><br/>                                   |
| [<span data-ttu-id="5f69f-121">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="5f69f-121">**IsPresent**</span></span>](extendedkeyusage-ispresent.md)<br/>   | <span data-ttu-id="5f69f-122">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5f69f-122">Read-only</span></span><br/> | <span data-ttu-id="5f69f-123">Ruft einen **booleschen** Wert ab, der angibt, ob die EKU-Erweiterung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5f69f-123">Retrieves a **Boolean** value that indicates whether the EKU extension is present.</span></span><br/> <span data-ttu-id="5f69f-124">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5f69f-124">This is the default property.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="5f69f-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f69f-125">Remarks</span></span>

<span data-ttu-id="5f69f-126">Das **extendedkeyusage** -Objekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5f69f-126">The **ExtendedKeyUsage** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f69f-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f69f-127">Requirements</span></span>



| <span data-ttu-id="5f69f-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f69f-128">Requirement</span></span> | <span data-ttu-id="5f69f-129">Wert</span><span class="sxs-lookup"><span data-stu-id="5f69f-129">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f69f-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="5f69f-130">End of client support</span></span><br/> | <span data-ttu-id="5f69f-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f69f-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5f69f-132">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="5f69f-132">End of server support</span></span><br/> | <span data-ttu-id="5f69f-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f69f-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5f69f-134">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="5f69f-134">Redistributable</span></span><br/>       | <span data-ttu-id="5f69f-135">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="5f69f-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5f69f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5f69f-136">DLL</span></span><br/>                   | <dl> <span data-ttu-id="5f69f-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f69f-137"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f69f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f69f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f69f-139">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="5f69f-139">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
