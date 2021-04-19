---
description: Ruft ein Zertifikat Objekt ab, das das indizierte Zertifikat der Auflistung darstellt. Dies ist die Standard Eigenschaft.
ms.assetid: 733f2b93-c059-4041-b7cd-8c20218f1462
title: Zertifikats. Item (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bbafaf20f74910e8ea5eb525f48374a2807fa030
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369259"
---
# <a name="certificatesitem-property"></a><span data-ttu-id="0c0f1-104">Zertifikats. Item (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0c0f1-104">Certificates.Item property</span></span>

<span data-ttu-id="0c0f1-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0c0f1-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0c0f1-106">Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="0c0f1-106">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0c0f1-107">Die **Item** -Eigenschaft ruft ein [**Zertifikat**](certificate.md) Objekt ab, das das indizierte Zertifikat der Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="0c0f1-107">The **Item** property retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="0c0f1-108">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0c0f1-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c0f1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c0f1-109">Syntax</span></span>


```VB
Certificates.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="0c0f1-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0c0f1-110">Property value</span></span>

<span data-ttu-id="0c0f1-111">Ein [**Zertifikat**](certificate.md) Objekt, das das indizierte Zertifikat darstellt.</span><span class="sxs-lookup"><span data-stu-id="0c0f1-111">A [**Certificate**](certificate.md) object that represents the indexed certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c0f1-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c0f1-112">Requirements</span></span>



| <span data-ttu-id="0c0f1-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c0f1-113">Requirement</span></span> | <span data-ttu-id="0c0f1-114">Wert</span><span class="sxs-lookup"><span data-stu-id="0c0f1-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c0f1-115">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0c0f1-115">End of client support</span></span><br/> | <span data-ttu-id="0c0f1-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c0f1-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0c0f1-117">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="0c0f1-117">End of server support</span></span><br/> | <span data-ttu-id="0c0f1-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c0f1-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0c0f1-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="0c0f1-119">Redistributable</span></span><br/>       | <span data-ttu-id="0c0f1-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c0f1-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0c0f1-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0c0f1-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0c0f1-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c0f1-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c0f1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c0f1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c0f1-124">**Zertifikate**</span><span class="sxs-lookup"><span data-stu-id="0c0f1-124">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
