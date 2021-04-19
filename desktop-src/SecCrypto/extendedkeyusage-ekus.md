---
description: Gibt die EKUs-Auflistung für das Zertifikat zurück.
ms.assetid: 64211a00-7d4d-4381-a134-9cd570ed7dbb
title: Extendedkeyusage. EKUs-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 24bcf7b4332e75afad0e21415a7dfe8eb690c32b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355870"
---
# <a name="extendedkeyusageekus-property"></a><span data-ttu-id="9bf6e-103">Extendedkeyusage. EKUs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9bf6e-103">ExtendedKeyUsage.EKUs property</span></span>

<span data-ttu-id="9bf6e-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9bf6e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9bf6e-105">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="9bf6e-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="9bf6e-106">Die **EKUs** -Eigenschaft gibt die [**EKUs**](ekus.md) -Sammlung für das Zertifikat zurück.</span><span class="sxs-lookup"><span data-stu-id="9bf6e-106">The **EKUs** property returns the [**EKUs**](ekus.md) collection for the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bf6e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bf6e-107">Syntax</span></span>


```VB
ExtendedKeyUsage.EKUs As EKUs
```



## <a name="property-value"></a><span data-ttu-id="9bf6e-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9bf6e-108">Property value</span></span>

<span data-ttu-id="9bf6e-109">Die [**EKUs**](ekus.md) -Auflistung, die die [**EKU**](eku.md) -Objekte für das Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="9bf6e-109">The [**EKUs**](ekus.md) collection that contains the [**EKU**](eku.md) objects for the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bf6e-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9bf6e-110">Requirements</span></span>



| <span data-ttu-id="9bf6e-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9bf6e-111">Requirement</span></span> | <span data-ttu-id="9bf6e-112">Wert</span><span class="sxs-lookup"><span data-stu-id="9bf6e-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf6e-113">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9bf6e-113">End of client support</span></span><br/> | <span data-ttu-id="9bf6e-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9bf6e-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9bf6e-115">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="9bf6e-115">End of server support</span></span><br/> | <span data-ttu-id="9bf6e-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9bf6e-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9bf6e-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="9bf6e-117">Redistributable</span></span><br/>       | <span data-ttu-id="9bf6e-118">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="9bf6e-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9bf6e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="9bf6e-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9bf6e-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bf6e-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bf6e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bf6e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bf6e-122">**Extendedkeyusage**</span><span class="sxs-lookup"><span data-stu-id="9bf6e-122">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 
