---
description: Ruft die Anzahl der policyinformation-Objekte in der Auflistung ab.
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: Certificatepolicies. Count-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0ee51e37b3fd4ac66c4e615eaf068edc98a64807
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364466"
---
# <a name="certificatepoliciescount-property"></a><span data-ttu-id="21762-103">Certificatepolicies. Count-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="21762-103">CertificatePolicies.Count property</span></span>

<span data-ttu-id="21762-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="21762-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="21762-105">Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um die Zertifikat Richtlinien abzurufen.\]</span><span class="sxs-lookup"><span data-stu-id="21762-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="21762-106">Die **count** -Eigenschaft ruft die Anzahl der [**policyinformation**](policyinformation.md) -Objekte in der-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="21762-106">The **Count** property retrieves the number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span>

<span data-ttu-id="21762-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="21762-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="21762-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="21762-108">Syntax</span></span>


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="21762-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="21762-109">Property value</span></span>

<span data-ttu-id="21762-110">Die Anzahl der [**policyinformation**](policyinformation.md) -Objekte in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="21762-110">The number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span> <span data-ttu-id="21762-111">Jedes **policyinformation** -Objekt stellt eine einzelne Zertifikat Richtlinie in der Sammlung dar.</span><span class="sxs-lookup"><span data-stu-id="21762-111">Each **PolicyInformation** object represents a single certificate policy in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="21762-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21762-112">Remarks</span></span>

<span data-ttu-id="21762-113">Die **count** -Eigenschaft kann verwendet werden, um das letzte [**policyinformation**](policyinformation.md) -Objekt in der Auflistung anzugeben, wenn ein bestimmtes **policyinformation** -Objekt mithilfe der [**certificatepolicies. Item**](certificatepolicies-item.md) -Eigenschaft abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="21762-113">The **Count** property can be used to specify the last [**PolicyInformation**](policyinformation.md) object in the collection when retrieving a specific **PolicyInformation** object using the [**CertificatePolicies.Item**](certificatepolicies-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="21762-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21762-114">Requirements</span></span>



| <span data-ttu-id="21762-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21762-115">Requirement</span></span> | <span data-ttu-id="21762-116">Wert</span><span class="sxs-lookup"><span data-stu-id="21762-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21762-117">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="21762-117">End of client support</span></span><br/> | <span data-ttu-id="21762-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21762-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="21762-119">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="21762-119">End of server support</span></span><br/> | <span data-ttu-id="21762-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21762-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="21762-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="21762-121">Redistributable</span></span><br/>       | <span data-ttu-id="21762-122">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="21762-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="21762-123">DLL</span><span class="sxs-lookup"><span data-stu-id="21762-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="21762-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21762-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
