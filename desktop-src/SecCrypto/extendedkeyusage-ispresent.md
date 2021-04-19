---
description: Gibt einen booleschen Wert zurück, der angibt, ob die EKU-Erweiterung vorhanden ist. Dies ist die Standard Eigenschaft.
ms.assetid: d7568525-1054-47e1-a176-f154792f9589
title: Extendedkeyusage. ispree sent (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 785fa3c973e7f90eeab20bd76826b9e5bf612891
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367691"
---
# <a name="extendedkeyusageispresent-property"></a><span data-ttu-id="68d76-104">Extendedkeyusage. ispree sent (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="68d76-104">ExtendedKeyUsage.IsPresent property</span></span>

<span data-ttu-id="68d76-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="68d76-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="68d76-106">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="68d76-106">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="68d76-107">Die **ispree sent** -Eigenschaft gibt einen booleschen Wert zurück, der angibt, ob die EKU-Erweiterung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="68d76-107">The **IsPresent** property returns a Boolean value that indicates whether the EKU extension is present.</span></span> <span data-ttu-id="68d76-108">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="68d76-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="68d76-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="68d76-109">Syntax</span></span>


```VB
ExtendedKeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="68d76-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="68d76-110">Property value</span></span>

<span data-ttu-id="68d76-111">**True** gibt an, dass die EKU-Erweiterung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="68d76-111">If **true**, the EKU extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="68d76-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68d76-112">Requirements</span></span>



| <span data-ttu-id="68d76-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68d76-113">Requirement</span></span> | <span data-ttu-id="68d76-114">Wert</span><span class="sxs-lookup"><span data-stu-id="68d76-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68d76-115">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="68d76-115">End of client support</span></span><br/> | <span data-ttu-id="68d76-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68d76-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="68d76-117">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="68d76-117">End of server support</span></span><br/> | <span data-ttu-id="68d76-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68d76-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="68d76-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="68d76-119">Redistributable</span></span><br/>       | <span data-ttu-id="68d76-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="68d76-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="68d76-121">DLL</span><span class="sxs-lookup"><span data-stu-id="68d76-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="68d76-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68d76-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68d76-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68d76-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68d76-124">**Extendedkeyusage**</span><span class="sxs-lookup"><span data-stu-id="68d76-124">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 
