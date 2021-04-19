---
description: Gibt eine OIDs-Auflistung zurück, die die Anwendungsrichtlinien darstellt, die zum Erstellen des Ketten Objekts verwendet werden.
ms.assetid: dca0acbf-e369-4216-a4f6-44ed965011d0
title: CertificateStatus. applicationpolicies-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b02503590a64c1c14e3f66dc5d07d9d61034bd60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354082"
---
# <a name="certificatestatusapplicationpolicies-method"></a><span data-ttu-id="8fb23-103">CertificateStatus. applicationpolicies-Methode</span><span class="sxs-lookup"><span data-stu-id="8fb23-103">CertificateStatus.ApplicationPolicies method</span></span>

<span data-ttu-id="8fb23-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8fb23-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="8fb23-105">Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="8fb23-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="8fb23-106">Die **applicationpolicies** -Methode gibt eine [**OIDs**](oids.md) -Auflistung zurück, die die Anwendungsrichtlinien darstellt, die zum Erstellen des [**Ketten**](chain.md) Objekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8fb23-106">The **ApplicationPolicies** method returns an [**OIDs**](oids.md) collection that represents the application policies used to create the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fb23-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fb23-107">Syntax</span></span>


```VB
CertificateStatus.ApplicationPolicies()
```



## <a name="parameters"></a><span data-ttu-id="8fb23-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fb23-108">Parameters</span></span>

<span data-ttu-id="8fb23-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8fb23-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8fb23-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8fb23-110">Return value</span></span>

<span data-ttu-id="8fb23-111">Eine [**OIDs**](oids.md) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="8fb23-111">An [**OIDs**](oids.md) collection.</span></span> <span data-ttu-id="8fb23-112">Jedes [**OID**](oid.md) -Objekt in der Auflistung stellt eine Anwendungsrichtlinien-OID dar.</span><span class="sxs-lookup"><span data-stu-id="8fb23-112">Each [**OID**](oid.md) object in the collection represents an application policy OID.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fb23-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fb23-113">Remarks</span></span>

<span data-ttu-id="8fb23-114">Fügen Sie der Sammlung Anwendungsrichtlinien-OIDs hinzu, um die Anwendungsrichtlinien anzugeben, die zum Erstellen der Zertifikats Vertrauenskette verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8fb23-114">Add application policy OIDs to the collection to specify the application policies that should be used to build the certificate trust chain.</span></span> <span data-ttu-id="8fb23-115">Wenn die Auflistung mindestens ein [**OID**](oid.md) -Objekt enthält, wird das von der [**CertificateStatus. EKU**](certificatestatus-eku.md) -Methode zurückgegebene [**EKU**](eku.md) -Objekt ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8fb23-115">If the collection contains at least one [**OID**](oid.md) object, the [**EKU**](eku.md) object returned by the [**CertificateStatus.EKU**](certificatestatus-eku.md) method is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fb23-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8fb23-116">Requirements</span></span>



| <span data-ttu-id="8fb23-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8fb23-117">Requirement</span></span> | <span data-ttu-id="8fb23-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8fb23-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb23-119">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="8fb23-119">End of client support</span></span><br/> | <span data-ttu-id="8fb23-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8fb23-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8fb23-121">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="8fb23-121">End of server support</span></span><br/> | <span data-ttu-id="8fb23-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fb23-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8fb23-123">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="8fb23-123">Redistributable</span></span><br/>       | <span data-ttu-id="8fb23-124">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="8fb23-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8fb23-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8fb23-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8fb23-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fb23-126"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
