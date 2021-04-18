---
description: Gibt eine OIDs-Auflistung zurück, die die für die Kette gültigen Zertifikat Richtlinie-OIDs darstellt.
ms.assetid: 18200003-f4f1-4cf3-af9a-bc223151ff68
title: 'IChain2:: certificatepolicies-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.CertificatePolicies
- IChain2.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e37abce9ea1aec5eb8adaf1d8eceeb3fac284fa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365366"
---
# <a name="ichain2certificatepolicies-method"></a><span data-ttu-id="35ae5-103">IChain2:: certificatepolicies-Methode</span><span class="sxs-lookup"><span data-stu-id="35ae5-103">IChain2::CertificatePolicies method</span></span>

<span data-ttu-id="35ae5-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="35ae5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="35ae5-105">Verwenden Sie stattdessen die [**X509Chain-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="35ae5-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="35ae5-106">Die **certificatepolicies** -Methode gibt eine [**OIDs**](oids.md) -Auflistung zurück, die die für die Kette gültigen Zertifikat Richtlinien OIDs darstellt.</span><span class="sxs-lookup"><span data-stu-id="35ae5-106">The **CertificatePolicies** method returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs valid for the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ae5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="35ae5-107">Syntax</span></span>


```VB
Chain.CertificatePolicies()
```



## <a name="parameters"></a><span data-ttu-id="35ae5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="35ae5-108">Parameters</span></span>

<span data-ttu-id="35ae5-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="35ae5-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="35ae5-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35ae5-110">Requirements</span></span>



| <span data-ttu-id="35ae5-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35ae5-111">Requirement</span></span> | <span data-ttu-id="35ae5-112">Wert</span><span class="sxs-lookup"><span data-stu-id="35ae5-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35ae5-113">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="35ae5-113">End of client support</span></span><br/> | <span data-ttu-id="35ae5-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35ae5-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="35ae5-115">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="35ae5-115">End of server support</span></span><br/> | <span data-ttu-id="35ae5-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35ae5-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="35ae5-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="35ae5-117">Redistributable</span></span><br/>       | <span data-ttu-id="35ae5-118">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="35ae5-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="35ae5-119">DLL</span><span class="sxs-lookup"><span data-stu-id="35ae5-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="35ae5-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35ae5-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
