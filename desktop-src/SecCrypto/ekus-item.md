---
description: Ruft das EKU-Objekt ab, das die indizierte Eigenschaft für erweiterte Schlüssel Verwendung (Extended Key Usage, EKU) darstellt.
ms.assetid: b8c12a7a-e836-48c2-958c-937b3723f85b
title: 'Iekus:: Item (Eigenschaft)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKUs.Item
- IEKUs.get_Item
- EKUs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e3eaf8d0b303207aae3ef78cc82771e1436b1027
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371673"
---
# <a name="iekusitem-property"></a><span data-ttu-id="72aa9-103">Iekus:: Item (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="72aa9-103">IEKUs::Item property</span></span>

<span data-ttu-id="72aa9-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="72aa9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="72aa9-105">Verwenden Sie stattdessen die [**X509ExtensionCollection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="72aa9-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="72aa9-106">Die **Item** -Eigenschaft ruft das [**EKU**](eku.md) -Objekt ab, das die Eigenschaft für die indizierte erweiterte Schlüssel Verwendung (EKU) darstellt.</span><span class="sxs-lookup"><span data-stu-id="72aa9-106">The **Item** property retrieves the [**EKU**](eku.md) object that represents the indexed extended key usage (EKU) property.</span></span>

<span data-ttu-id="72aa9-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="72aa9-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="72aa9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="72aa9-108">Syntax</span></span>


```VB
EKUs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="72aa9-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="72aa9-109">Property value</span></span>

<span data-ttu-id="72aa9-110">Ein [**EKU**](eku.md) -Objekt, das die indizierte EKU-Eigenschaft (Extended Key Usage) darstellt.</span><span class="sxs-lookup"><span data-stu-id="72aa9-110">An [**EKU**](eku.md) object that represents the indexed extended key usage (EKU) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="72aa9-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72aa9-111">Requirements</span></span>



| <span data-ttu-id="72aa9-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72aa9-112">Requirement</span></span> | <span data-ttu-id="72aa9-113">Wert</span><span class="sxs-lookup"><span data-stu-id="72aa9-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72aa9-114">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="72aa9-114">End of client support</span></span><br/> | <span data-ttu-id="72aa9-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72aa9-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="72aa9-116">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="72aa9-116">End of server support</span></span><br/> | <span data-ttu-id="72aa9-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72aa9-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="72aa9-118">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="72aa9-118">Redistributable</span></span><br/>       | <span data-ttu-id="72aa9-119">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="72aa9-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="72aa9-120">DLL</span><span class="sxs-lookup"><span data-stu-id="72aa9-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="72aa9-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72aa9-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72aa9-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72aa9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72aa9-123">**EKUs**</span><span class="sxs-lookup"><span data-stu-id="72aa9-123">**EKUs**</span></span>](ekus.md)
</dt> </dl>

 

 
