---
description: Ruft die OID der Richtlinie ab. Dies ist die Standard Eigenschaft.
ms.assetid: c78bbbcb-befd-491c-afbd-80c3ba124d29
title: Policyinformation. Oid (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9acab40130ef6c55bf014058b3e5a6d935ed8a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365925"
---
# <a name="policyinformationoid-property"></a><span data-ttu-id="6d61a-104">Policyinformation. Oid (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6d61a-104">PolicyInformation.OID property</span></span>

<span data-ttu-id="6d61a-105">\[Die **OID** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6d61a-105">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6d61a-106">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung zu verarbeiten.\]</span><span class="sxs-lookup"><span data-stu-id="6d61a-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="6d61a-107">Die **OID** -Eigenschaft ruft die OID der Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="6d61a-107">The **OID** property retrieves the policy's OID.</span></span> <span data-ttu-id="6d61a-108">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6d61a-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d61a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d61a-109">Syntax</span></span>


```VB
PolicyInformation.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="6d61a-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6d61a-110">Property value</span></span>

<span data-ttu-id="6d61a-111">Der Objekt Bezeichner der Richtlinie als [**OID**](oid.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="6d61a-111">The policy's object identifier as an [**OID**](oid.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d61a-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d61a-112">Requirements</span></span>



| <span data-ttu-id="6d61a-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d61a-113">Requirement</span></span> | <span data-ttu-id="6d61a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6d61a-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d61a-115">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="6d61a-115">Redistributable</span></span><br/> | <span data-ttu-id="6d61a-116">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="6d61a-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6d61a-117">DLL</span><span class="sxs-lookup"><span data-stu-id="6d61a-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="6d61a-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d61a-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d61a-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d61a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d61a-120">**Policyinformation**</span><span class="sxs-lookup"><span data-stu-id="6d61a-120">**PolicyInformation**</span></span>](policyinformation.md)
</dt> </dl>

 

 
