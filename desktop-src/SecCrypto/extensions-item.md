---
description: Die Item-Eigenschaft ruft eine Erweiterung nach Index aus der-Auflistung ab. Dies ist die Standard Eigenschaft.
ms.assetid: 0242dc14-abf2-49df-b75a-9005b2376cfc
title: Extensions. Item (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b2cefe9ac1dd278c17161cc8e2349c051dccabff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369470"
---
# <a name="extensionsitem-property"></a><span data-ttu-id="33b5b-104">Extensions. Item (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="33b5b-104">Extensions.Item property</span></span>

<span data-ttu-id="33b5b-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="33b5b-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="33b5b-106">Verwenden Sie stattdessen die [**X509ExtensionCollection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="33b5b-106">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="33b5b-107">Die **Item** -Eigenschaft ruft eine Erweiterung nach Index aus der-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="33b5b-107">The **Item** property retrieves an extension, by index, from the collection.</span></span> <span data-ttu-id="33b5b-108">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="33b5b-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="33b5b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="33b5b-109">Syntax</span></span>


```VB
Extensions.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="33b5b-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="33b5b-110">Property value</span></span>

<span data-ttu-id="33b5b-111">Ein [**Erweiterungs**](extension.md) Objekt, das die indizierte Zertifikats Erweiterung der Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="33b5b-111">An [**Extension**](extension.md) object that represents the indexed certificate extension of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="33b5b-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33b5b-112">Requirements</span></span>



| <span data-ttu-id="33b5b-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33b5b-113">Requirement</span></span> | <span data-ttu-id="33b5b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="33b5b-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33b5b-115">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="33b5b-115">End of client support</span></span><br/> | <span data-ttu-id="33b5b-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33b5b-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="33b5b-117">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="33b5b-117">End of server support</span></span><br/> | <span data-ttu-id="33b5b-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33b5b-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="33b5b-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="33b5b-119">Redistributable</span></span><br/>       | <span data-ttu-id="33b5b-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="33b5b-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="33b5b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="33b5b-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="33b5b-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33b5b-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33b5b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33b5b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33b5b-124">**Erweiterungen**</span><span class="sxs-lookup"><span data-stu-id="33b5b-124">**Extensions**</span></span>](extensions.md)
</dt> </dl>

 

 
