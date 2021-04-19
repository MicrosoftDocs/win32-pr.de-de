---
description: Ruft eine Auflistung der Qualifizierer der Richtlinie ab.
ms.assetid: aa5e2225-0a39-40bc-868c-d96f5953edaa
title: Policyinformation. qualifizierungseigenschaft (IADs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 89f24e21acd24cbcaa021f7c668fc8c208102c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360291"
---
# <a name="policyinformationqualifiers-property"></a><span data-ttu-id="8d731-103">Policyinformation. qualifizierungseigenschaft</span><span class="sxs-lookup"><span data-stu-id="8d731-103">PolicyInformation.Qualifiers property</span></span>

<span data-ttu-id="8d731-104">\[Die Eigenschaft **Qualifizierer** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="8d731-104">\[The **Qualifiers** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8d731-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung zu verarbeiten.\]</span><span class="sxs-lookup"><span data-stu-id="8d731-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="8d731-106">Die **qualifizierereigenschaft** Ruft eine Auflistung der Qualifizierer der Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="8d731-106">The **Qualifiers** property retrieves a collection of the policy's qualifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d731-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d731-107">Syntax</span></span>


```VB
PolicyInformation.Qualifiers As Qualifiers
```



## <a name="property-value"></a><span data-ttu-id="8d731-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8d731-108">Property value</span></span>

<span data-ttu-id="8d731-109">Der CPS-Zeiger (Certification Practice Statement) der Richtlinie oder Benutzer Qualifizierer [](qualifiers.md) als qualifiziererobjekt.</span><span class="sxs-lookup"><span data-stu-id="8d731-109">The policy's Certification Practice Statement (CPS) pointer or user notice qualifiers, as a [**Qualifiers**](qualifiers.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d731-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d731-110">Requirements</span></span>



| <span data-ttu-id="8d731-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d731-111">Requirement</span></span> | <span data-ttu-id="8d731-112">Wert</span><span class="sxs-lookup"><span data-stu-id="8d731-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d731-113">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="8d731-113">Redistributable</span></span><br/> | <span data-ttu-id="8d731-114">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="8d731-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8d731-115">Header</span><span class="sxs-lookup"><span data-stu-id="8d731-115">Header</span></span><br/>          | <dl> <span data-ttu-id="8d731-116"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d731-116"><dt>Iads.h</dt></span></span> </dl>      |
| <span data-ttu-id="8d731-117">DLL</span><span class="sxs-lookup"><span data-stu-id="8d731-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="8d731-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d731-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d731-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d731-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d731-120">**Policyinformation**</span><span class="sxs-lookup"><span data-stu-id="8d731-120">**PolicyInformation**</span></span>](policyinformation.md)
</dt> </dl>

 

 
