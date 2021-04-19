---
description: Legt die Uhrzeit fest, zu der das Zertifikat überprüft wurde, oder ruft diese ab.
ms.assetid: 1bd17df3-2fa1-4b99-ab00-659b4ad5fcd9
title: CertificateStatus. VerificationTime-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.VerificationTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 178402861c9830efbea78a31081ae7e8b31800b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350756"
---
# <a name="certificatestatusverificationtime-property"></a><span data-ttu-id="b4f57-103">CertificateStatus. VerificationTime-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b4f57-103">CertificateStatus.VerificationTime property</span></span>

<span data-ttu-id="b4f57-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b4f57-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b4f57-105">Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="b4f57-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b4f57-106">Die **VerificationTime** -Eigenschaft legt die Uhrzeit fest, zu der das Zertifikat überprüft wurde, oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="b4f57-106">The **VerificationTime** property sets or retrieves the time that the certificate was verified.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4f57-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4f57-107">Syntax</span></span>


```VB
CertificateStatus.VerificationTime As Date
```



## <a name="property-value"></a><span data-ttu-id="b4f57-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b4f57-108">Property value</span></span>

<span data-ttu-id="b4f57-109">Der Zeitpunkt, zu dem das Zertifikat überprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="b4f57-109">The time that the certificate was verified.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4f57-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4f57-110">Remarks</span></span>

<span data-ttu-id="b4f57-111">Wenn diese Eigenschaft nicht festgelegt ist, wird die aktuelle Uhrzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="b4f57-111">If this property is not set, the current time is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4f57-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4f57-112">Requirements</span></span>



| <span data-ttu-id="b4f57-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4f57-113">Requirement</span></span> | <span data-ttu-id="b4f57-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b4f57-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f57-115">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b4f57-115">End of client support</span></span><br/> | <span data-ttu-id="b4f57-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4f57-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b4f57-117">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="b4f57-117">End of server support</span></span><br/> | <span data-ttu-id="b4f57-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4f57-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b4f57-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="b4f57-119">Redistributable</span></span><br/>       | <span data-ttu-id="b4f57-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="b4f57-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b4f57-121">DLL</span><span class="sxs-lookup"><span data-stu-id="b4f57-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b4f57-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4f57-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
