---
description: Gibt eine OIDs-Auflistung zurück, die die zum Erstellen des Ketten Objekts verwendeten Zertifikat Richtlinien darstellt.
ms.assetid: 7fe7d3ea-28fc-4c0a-9b43-a97518ac65db
title: CertificateStatus. certificatepolicies-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98c9e22c0cad40252cc9eebebf9aa32dc4d89b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364942"
---
# <a name="certificatestatuscertificatepolicies-method"></a><span data-ttu-id="d933f-103">CertificateStatus. certificatepolicies-Methode</span><span class="sxs-lookup"><span data-stu-id="d933f-103">CertificateStatus.CertificatePolicies method</span></span>

<span data-ttu-id="d933f-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d933f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d933f-105">Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="d933f-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d933f-106">Die **certificatepolicies** -Methode gibt eine [**OIDs**](oids.md) -Auflistung zurück, die die Zertifikat Richtlinien darstellt, die zum Erstellen des [**Ketten**](chain.md) Objekts verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d933f-106">The **CertificatePolicies** method returns an [**OIDs**](oids.md) collection that represents the certificate policies used to create the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d933f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d933f-107">Syntax</span></span>


```VB
CertificateStatus.CertificatePolicies()
```



## <a name="parameters"></a><span data-ttu-id="d933f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d933f-108">Parameters</span></span>

<span data-ttu-id="d933f-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d933f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d933f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d933f-110">Return value</span></span>

<span data-ttu-id="d933f-111">Eine [**OIDs**](oids.md) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="d933f-111">An [**OIDs**](oids.md) collection.</span></span> <span data-ttu-id="d933f-112">Jedes [**OID**](oid.md) -Objekt in der Auflistung stellt eine Zertifikat Richtlinien-OID dar.</span><span class="sxs-lookup"><span data-stu-id="d933f-112">Each [**OID**](oid.md) object in the collection represents a certificate policy OID.</span></span>

## <a name="remarks"></a><span data-ttu-id="d933f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d933f-113">Remarks</span></span>

<span data-ttu-id="d933f-114">Fügen Sie der Sammlung Zertifikats Richtlinie hinzu, um die Zertifikat Richtlinien anzugeben, die zum Erstellen der Zertifikats Vertrauenskette verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d933f-114">Add certificate policy OIDs to the collection to specify the certificate policies that should be used to build the certificate trust chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="d933f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d933f-115">Requirements</span></span>



| <span data-ttu-id="d933f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d933f-116">Requirement</span></span> | <span data-ttu-id="d933f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d933f-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d933f-118">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d933f-118">End of client support</span></span><br/> | <span data-ttu-id="d933f-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d933f-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d933f-120">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="d933f-120">End of server support</span></span><br/> | <span data-ttu-id="d933f-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d933f-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d933f-122">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d933f-122">Redistributable</span></span><br/>       | <span data-ttu-id="d933f-123">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="d933f-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d933f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d933f-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d933f-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d933f-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
