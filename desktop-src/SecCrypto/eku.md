---
description: Stellt eine einzelne EKU-Eigenschaft (Extended Key Usage) eines Zertifikats dar.
ms.assetid: 08eb7c77-0224-4ab5-99e7-edf18eb23c60
title: EKU-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ff397ae747ecd09dd1292e5c15eb4291692d9651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365743"
---
# <a name="eku-object"></a><span data-ttu-id="d2b89-103">EKU-Objekt</span><span class="sxs-lookup"><span data-stu-id="d2b89-103">EKU object</span></span>

<span data-ttu-id="d2b89-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d2b89-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d2b89-105">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="d2b89-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d2b89-106">Das **EKU** -Objekt stellt eine einzelne EKU (Extended Key Usage)-Eigenschaft eines Zertifikats dar.</span><span class="sxs-lookup"><span data-stu-id="d2b89-106">The **EKU** object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="d2b89-107">Member</span><span class="sxs-lookup"><span data-stu-id="d2b89-107">Members</span></span>

<span data-ttu-id="d2b89-108">Das **EKU** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d2b89-108">The **EKU** object has these types of members:</span></span>

-   [<span data-ttu-id="d2b89-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d2b89-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d2b89-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d2b89-110">Properties</span></span>

<span data-ttu-id="d2b89-111">Das **EKU** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d2b89-111">The **EKU** object has these properties.</span></span>



| <span data-ttu-id="d2b89-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d2b89-112">Property</span></span>                            | <span data-ttu-id="d2b89-113">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="d2b89-113">Access type</span></span>           | <span data-ttu-id="d2b89-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2b89-114">Description</span></span>                                                                                                                                                                                                   |
|:------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2b89-115">**Name**</span><span class="sxs-lookup"><span data-stu-id="d2b89-115">**Name**</span></span>](eku-name.md)<br/> | <span data-ttu-id="d2b89-116">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2b89-116">Read/write</span></span><br/> | <span data-ttu-id="d2b89-117">Legt einen Enumerationswert fest, der den CAPICOM-Namen der EKU angibt, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="d2b89-117">Sets or retrieves an enumeration value that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="d2b89-118">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d2b89-118">This is the default property.</span></span><br/>                                                                                   |
| [<span data-ttu-id="d2b89-119">**OID**</span><span class="sxs-lookup"><span data-stu-id="d2b89-119">**OID**</span></span>](eku-oid.md)<br/>   | <span data-ttu-id="d2b89-120">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2b89-120">Read/write</span></span><br/> | <span data-ttu-id="d2b89-121">Legt eine Zeichenfolge fest oder ruft eine Zeichenfolge ab, die einen in Wincrypt. h definierten EKU- [*Objekt Bezeichner*](../secgloss/o-gly.md) (OID)-Zeichen folgen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="d2b89-121">Sets or retrieves a string that contains an EKU [*object identifier*](../secgloss/o-gly.md) (OID) string value as defined in Wincrypt.h.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d2b89-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2b89-122">Remarks</span></span>

<span data-ttu-id="d2b89-123">Das **EKU** -Objekt wird von der folgenden Auflistung und Eigenschaft verwendet:</span><span class="sxs-lookup"><span data-stu-id="d2b89-123">The **EKU** object is used by the following collection and property:</span></span>

-   <span data-ttu-id="d2b89-124">[**EKUs**](ekus.md) -Sammlung</span><span class="sxs-lookup"><span data-stu-id="d2b89-124">[**EKUs**](ekus.md) collection</span></span>
-   <span data-ttu-id="d2b89-125">[**CertificateStatus. EKU**](certificatestatus-eku.md) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d2b89-125">[**CertificateStatus.EKU**](certificatestatus-eku.md) property</span></span>

<span data-ttu-id="d2b89-126">Das **EKU** -Objekt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d2b89-126">The **EKU** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2b89-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2b89-127">Requirements</span></span>



| <span data-ttu-id="d2b89-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2b89-128">Requirement</span></span> | <span data-ttu-id="d2b89-129">Wert</span><span class="sxs-lookup"><span data-stu-id="d2b89-129">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b89-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d2b89-130">End of client support</span></span><br/> | <span data-ttu-id="d2b89-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2b89-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d2b89-132">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="d2b89-132">End of server support</span></span><br/> | <span data-ttu-id="d2b89-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2b89-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d2b89-134">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d2b89-134">Redistributable</span></span><br/>       | <span data-ttu-id="d2b89-135">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="d2b89-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d2b89-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d2b89-136">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d2b89-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2b89-137"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
