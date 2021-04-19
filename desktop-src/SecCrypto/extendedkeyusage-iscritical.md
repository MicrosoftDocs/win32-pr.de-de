---
description: Gibt einen booleschen Wert zurück, der angibt, ob die EKU-Erweiterung als kritisch markiert ist.
ms.assetid: f6d2a2e0-512b-44f2-a7d9-9ad661398aa8
title: Extendedkeyusage. IsCritical (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5331922567af3b9a34517ab5059fa03ad9904270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373717"
---
# <a name="extendedkeyusageiscritical-property"></a><span data-ttu-id="a0200-103">Extendedkeyusage. IsCritical (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a0200-103">ExtendedKeyUsage.IsCritical property</span></span>

<span data-ttu-id="a0200-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a0200-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a0200-105">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="a0200-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a0200-106">Die **IsCritical** -Eigenschaft gibt einen booleschen Wert zurück, der angibt, ob die EKU-Erweiterung als kritisch markiert ist.</span><span class="sxs-lookup"><span data-stu-id="a0200-106">The **IsCritical** property returns a Boolean value that indicates whether the EKU extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0200-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0200-107">Syntax</span></span>


```VB
ExtendedKeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a0200-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a0200-108">Property value</span></span>

<span data-ttu-id="a0200-109">**True** gibt an, dass die EKU-Erweiterung als kritisch markiert ist.</span><span class="sxs-lookup"><span data-stu-id="a0200-109">If **true**, the EKU extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0200-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0200-110">Requirements</span></span>



| <span data-ttu-id="a0200-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0200-111">Requirement</span></span> | <span data-ttu-id="a0200-112">Wert</span><span class="sxs-lookup"><span data-stu-id="a0200-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0200-113">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a0200-113">End of client support</span></span><br/> | <span data-ttu-id="a0200-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0200-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a0200-115">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="a0200-115">End of server support</span></span><br/> | <span data-ttu-id="a0200-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0200-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a0200-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="a0200-117">Redistributable</span></span><br/>       | <span data-ttu-id="a0200-118">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="a0200-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a0200-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a0200-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a0200-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0200-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0200-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0200-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0200-122">**Extendedkeyusage**</span><span class="sxs-lookup"><span data-stu-id="a0200-122">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 
