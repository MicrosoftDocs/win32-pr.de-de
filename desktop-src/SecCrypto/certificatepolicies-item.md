---
description: Ruft das policyinformation-Objekt ab, das die indizierte Richtlinie darstellt. Dies ist die Standard Eigenschaft.
ms.assetid: 0143629a-97cf-43f4-8f96-774f0f5cfeca
title: Certificatepolicies. Item (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a41cfb88f5f3ad59a8dbf62c85eca2a13c69f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365659"
---
# <a name="certificatepoliciesitem-property"></a><span data-ttu-id="26e6e-104">Certificatepolicies. Item (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="26e6e-104">CertificatePolicies.Item property</span></span>

<span data-ttu-id="26e6e-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="26e6e-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="26e6e-106">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um die Zertifikat Richtlinien abzurufen.\]</span><span class="sxs-lookup"><span data-stu-id="26e6e-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="26e6e-107">Die **Item** -Eigenschaft ruft das [**policyinformation**](policyinformation.md) -Objekt ab, das die indizierte Richtlinie darstellt.</span><span class="sxs-lookup"><span data-stu-id="26e6e-107">The **Item** property retrieves the [**PolicyInformation**](policyinformation.md) object that represents the indexed policy.</span></span> <span data-ttu-id="26e6e-108">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="26e6e-108">This is the default property.</span></span>

<span data-ttu-id="26e6e-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="26e6e-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="26e6e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="26e6e-110">Syntax</span></span>


```VB
CertificatePolicies.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="26e6e-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="26e6e-111">Property value</span></span>

<span data-ttu-id="26e6e-112">Ein [**policyinformation**](policyinformation.md) -Objekt, das die indizierte Richtlinie darstellt.</span><span class="sxs-lookup"><span data-stu-id="26e6e-112">A [**PolicyInformation**](policyinformation.md) object that represents the indexed policy.</span></span>

## <a name="requirements"></a><span data-ttu-id="26e6e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26e6e-113">Requirements</span></span>



| <span data-ttu-id="26e6e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26e6e-114">Requirement</span></span> | <span data-ttu-id="26e6e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="26e6e-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26e6e-116">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="26e6e-116">End of client support</span></span><br/> | <span data-ttu-id="26e6e-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26e6e-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="26e6e-118">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="26e6e-118">End of server support</span></span><br/> | <span data-ttu-id="26e6e-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26e6e-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="26e6e-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="26e6e-120">Redistributable</span></span><br/>       | <span data-ttu-id="26e6e-121">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="26e6e-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="26e6e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="26e6e-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="26e6e-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26e6e-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
