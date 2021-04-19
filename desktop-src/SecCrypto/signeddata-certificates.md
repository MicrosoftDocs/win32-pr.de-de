---
description: Ruft die dem SignedData-Objekt zugeordnete Zertifikats Auflistung ab. Nach dem abrufen können die einzelnen Zertifikat Objekte in der Auflistung aufgelistet werden.
ms.assetid: 94741fee-2462-4a18-bc14-c52e9cac374b
title: SignedData. Zertifikats (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 55c0fe432794289fabe67b37deeedfac43f7a7d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354162"
---
# <a name="signeddatacertificates-property"></a><span data-ttu-id="3c4d2-104">SignedData. Zertifikats (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3c4d2-104">SignedData.Certificates property</span></span>

<span data-ttu-id="3c4d2-105">\[Die Eigenschaft **Zertifikate** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="3c4d2-105">\[The **Certificates** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3c4d2-106">Verwenden Sie stattdessen die [**SignedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="3c4d2-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="3c4d2-107">Mit der Eigenschaft **Zertifikate** wird die dem [**SignedData**](signeddata.md) -Objekt zugeordnete [**Zertifikats**](certificates.md) Sammlung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3c4d2-107">The **Certificates** property retrieves the [**Certificates**](certificates.md) collection that is associated with the [**SignedData**](signeddata.md) object.</span></span> <span data-ttu-id="3c4d2-108">Nach dem abrufen können die einzelnen [**Zertifikat**](certificate.md) Objekte in der Auflistung aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="3c4d2-108">After being retrieved, the individual [**Certificate**](certificate.md) objects in the collection can be enumerated.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c4d2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c4d2-109">Syntax</span></span>


```VB
SignedData.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="3c4d2-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3c4d2-110">Property value</span></span>

<span data-ttu-id="3c4d2-111">Die dem [**SignedData**](signeddata.md) -Objekt zugeordnete [**Zertifikats**](certificates.md) Auflistung.</span><span class="sxs-lookup"><span data-stu-id="3c4d2-111">The [**Certificates**](certificates.md) collection that is associated with the [**SignedData**](signeddata.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c4d2-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c4d2-112">Requirements</span></span>



| <span data-ttu-id="3c4d2-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c4d2-113">Requirement</span></span> | <span data-ttu-id="3c4d2-114">Wert</span><span class="sxs-lookup"><span data-stu-id="3c4d2-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c4d2-115">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="3c4d2-115">Redistributable</span></span><br/> | <span data-ttu-id="3c4d2-116">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="3c4d2-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3c4d2-117">DLL</span><span class="sxs-lookup"><span data-stu-id="3c4d2-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="3c4d2-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c4d2-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c4d2-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c4d2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c4d2-120">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="3c4d2-120">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
