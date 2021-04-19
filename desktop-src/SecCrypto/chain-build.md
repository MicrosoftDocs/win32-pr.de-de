---
description: Erstellt eine Zertifikat Überprüfungs Kette von einem Endzertifikat zum vertrauenswürdigen Stamm Zertifikat und gibt einen booleschen Wert zurück, der die Gesamt Gültigkeit der Kette angibt.
ms.assetid: 878f09ba-d79b-4f14-b4f6-ecb54771f56f
title: 'IChain2:: Build-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.Build
- IChain2.Build
- IChain.Build
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66ad51d94fdbd361a34e25b4b76289139abb87f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353784"
---
# <a name="ichain2build-method"></a><span data-ttu-id="c6785-103">IChain2:: Build-Methode</span><span class="sxs-lookup"><span data-stu-id="c6785-103">IChain2::Build method</span></span>

<span data-ttu-id="c6785-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c6785-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c6785-105">Verwenden Sie stattdessen die [**X509Chain-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="c6785-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c6785-106">Die **Build** -Methode erstellt eine Zertifikat Überprüfungs Kette von einem Endzertifikat zum vertrauenswürdigen Stamm [*Zertifikat*](../secgloss/r-gly.md) und gibt einen booleschen Wert zurück, der die Gesamt Gültigkeit der Kette angibt.</span><span class="sxs-lookup"><span data-stu-id="c6785-106">The **Build** method builds a certificate verification chain from an end certificate to the trusted [*root certificate*](../secgloss/r-gly.md) and returns a Boolean value that indicates the overall validity of the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6785-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6785-107">Syntax</span></span>


```VB
Chain.Build( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="c6785-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6785-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6785-109">*Zertifikat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6785-109">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6785-110">Ein [**Zertifikat**](certificate.md) Objekt, das das Endzertifikat darstellt, auf dem die Überprüfungs Kette erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6785-110">A [**Certificate**](certificate.md) object that represents the end certificate upon which the verification chain is to be built.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6785-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6785-111">Return value</span></span>

<span data-ttu-id="c6785-112">Ein boolescher Wert, der die Gesamt Gültigkeit der Kette angibt.</span><span class="sxs-lookup"><span data-stu-id="c6785-112">A Boolean value that indicates the overall validity of the chain.</span></span> <span data-ttu-id="c6785-113">Die Gesamt Gültigkeit basiert auf der Richtlinie für die Gültigkeitsprüfung.</span><span class="sxs-lookup"><span data-stu-id="c6785-113">Overall validity is based on the validity checking policy in place.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6785-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6785-114">Remarks</span></span>

<span data-ttu-id="c6785-115">Die Kette wird mit der Eigenschaft [**CertificateStatus. checkflag**](certificatestatus-checkflag.md) sowie mit den von einem [**CertificateStatus**](certificatestatus.md) -Objekt angegebenen Anwendungs-und Zertifikat Richtlinien erstellt.</span><span class="sxs-lookup"><span data-stu-id="c6785-115">The chain is built using the [**CertificateStatus.CheckFlag**](certificatestatus-checkflag.md) property as well as application and certificate policies specified by a [**CertificateStatus**](certificatestatus.md) object.</span></span> <span data-ttu-id="c6785-116">Die zurückgegebene Auflistung ist geordnet. das erste Zertifikat in der Sammlung, "Certificate **. Item**(1)", ist das Endzertifikat der Kette.</span><span class="sxs-lookup"><span data-stu-id="c6785-116">The returned collection is ordered; the first certificate in the collection, **Certificates.Item**(1), is the end certificate of the chain.</span></span> <span data-ttu-id="c6785-117">Das letzte Zertifikat in der Sammlung, "Certificate **. Item**" ("**Zertifikate. count**"), ist das Stamm [*Zertifikat*](../secgloss/r-gly.md) der Kette.</span><span class="sxs-lookup"><span data-stu-id="c6785-117">The last certificate in the collection, **Certificates.Item**(**Certificates.Count**), is the [*root certificate*](../secgloss/r-gly.md) of the chain.</span></span> <span data-ttu-id="c6785-118">" **Zertifikate. Item**(0)" stellt die gesamte Kette dar.</span><span class="sxs-lookup"><span data-stu-id="c6785-118">**Certificates.Item**(0) represents the entire chain.</span></span>

<span data-ttu-id="c6785-119">Jedes Mal, wenn die **Chain. Build** -Methode aufgerufen wird, wird der [*Zustand*](../secgloss/s-gly.md) des [**Kette**](chain.md) -Objekts zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="c6785-119">Each time the **Chain.Build** method is called, the [*state*](../secgloss/s-gly.md) of the [**Chain**](chain.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6785-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6785-120">Requirements</span></span>



| <span data-ttu-id="c6785-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6785-121">Requirement</span></span> | <span data-ttu-id="c6785-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c6785-122">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6785-123">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c6785-123">End of client support</span></span><br/> | <span data-ttu-id="c6785-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6785-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c6785-125">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c6785-125">End of server support</span></span><br/> | <span data-ttu-id="c6785-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6785-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c6785-127">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c6785-127">Redistributable</span></span><br/>       | <span data-ttu-id="c6785-128">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="c6785-128">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c6785-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c6785-129">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c6785-130"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6785-130"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6785-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6785-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6785-132">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="c6785-132">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="c6785-133">**Ketten**</span><span class="sxs-lookup"><span data-stu-id="c6785-133">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
