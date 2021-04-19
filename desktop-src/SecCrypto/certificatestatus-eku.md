---
description: Gibt das EKU-Objekt zurück, das zum Erstellen des Ketten Objekts verwendet wird.
ms.assetid: d02f1614-6a4f-4c60-b406-ce174a99e9a5
title: CertificateStatus. EKU-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d386251c6d7f674d3850de275559bcb87ea6d61e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369951"
---
# <a name="certificatestatuseku-method"></a><span data-ttu-id="3e5c7-103">CertificateStatus. EKU-Methode</span><span class="sxs-lookup"><span data-stu-id="3e5c7-103">CertificateStatus.EKU method</span></span>

<span data-ttu-id="3e5c7-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3e5c7-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3e5c7-105">Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="3e5c7-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="3e5c7-106">Die **EKU** -Methode gibt das [**EKU**](eku.md) -Objekt zurück, das zum Erstellen des [**Ketten**](chain.md) Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e5c7-106">The **EKU** method returns the [**EKU**](eku.md) object used to build the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e5c7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e5c7-107">Syntax</span></span>


```VB
CertificateStatus.EKU()
```



## <a name="parameters"></a><span data-ttu-id="3e5c7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e5c7-108">Parameters</span></span>

<span data-ttu-id="3e5c7-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3e5c7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3e5c7-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e5c7-110">Return value</span></span>

<span data-ttu-id="3e5c7-111">Diese Methode gibt ein [**EKU**](eku.md) -Objekt zurück, das die erweiterte Schlüssel Verwendung des [*Zertifikats*](../secgloss/c-gly.md)angibt.</span><span class="sxs-lookup"><span data-stu-id="3e5c7-111">This method returns an [**EKU**](eku.md) object that indicates the extended key usage setting of the [*certificate*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="3e5c7-112">Mit der EKU-Einstellung wird die gültige Verwendung eines Zertifikats festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3e5c7-112">The EKU setting establishes a certificate's valid use.</span></span> <span data-ttu-id="3e5c7-113">Für jedes Zertifikat kann nur ein einzelnes **EKU** -Objekt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3e5c7-113">Only a single **EKU** object can be set for each certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e5c7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e5c7-114">Remarks</span></span>

<span data-ttu-id="3e5c7-115">Die [**CertificateStatus. applicationpolicies**](certificatestatus-applicationpolicies.md) -Methode bietet die gleiche Funktionalität wie diese Methode, ermöglicht jedoch, dass viele Einstellungen anstelle von nur einer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3e5c7-115">The [**CertificateStatus.ApplicationPolicies**](certificatestatus-applicationpolicies.md) method provides the same functionality as this method but allows many settings to be specified instead of only one.</span></span> <span data-ttu-id="3e5c7-116">Wenn die von der **applicationpolicies** -Methode zurückgegebene [**OIDs**](oids.md) -Auflistung ein oder mehrere [**OID**](oid.md) -Objekte enthält, wird das von dieser Methode zurückgegebene [**EKU**](eku.md) -Objekt ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3e5c7-116">If the [**OIDs**](oids.md) collection returned by the **ApplicationPolicies** method contains one or more [**OID**](oid.md) objects, the [**EKU**](eku.md) object returned by this method is ignored.</span></span> <span data-ttu-id="3e5c7-117">Verwenden Sie die **applicationpolicies** -Methode anstelle dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="3e5c7-117">Use the **ApplicationPolicies** method instead of this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e5c7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e5c7-118">Requirements</span></span>



| <span data-ttu-id="3e5c7-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e5c7-119">Requirement</span></span> | <span data-ttu-id="3e5c7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3e5c7-120">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5c7-121">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3e5c7-121">End of client support</span></span><br/> | <span data-ttu-id="3e5c7-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e5c7-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3e5c7-123">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="3e5c7-123">End of server support</span></span><br/> | <span data-ttu-id="3e5c7-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e5c7-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3e5c7-125">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="3e5c7-125">Redistributable</span></span><br/>       | <span data-ttu-id="3e5c7-126">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5c7-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3e5c7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3e5c7-127">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3e5c7-128"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e5c7-128"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e5c7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e5c7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e5c7-130">**CertificateStatus**</span><span class="sxs-lookup"><span data-stu-id="3e5c7-130">**CertificateStatus**</span></span>](certificatestatus.md)
</dt> <dt>

[<span data-ttu-id="3e5c7-131">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="3e5c7-131">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="3e5c7-132">**EKU**</span><span class="sxs-lookup"><span data-stu-id="3e5c7-132">**EKU**</span></span>](eku.md)
</dt> </dl>

 

 
