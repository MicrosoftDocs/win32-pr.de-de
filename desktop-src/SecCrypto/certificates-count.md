---
description: Ruft die Anzahl der Zertifikat Objekte in der Auflistung ab.
ms.assetid: 95931721-3b0c-4915-805f-039d1d5510fa
title: Zertifikats. Count-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a67554530ce8c8dfdc1bfcfba1198cf778397ac2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361504"
---
# <a name="certificatescount-property"></a><span data-ttu-id="e1890-103">Zertifikats. Count-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e1890-103">Certificates.Count property</span></span>

<span data-ttu-id="e1890-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e1890-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e1890-105">Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="e1890-105">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e1890-106">Die **count** -Eigenschaft ruft die Anzahl der [**Zertifikat**](certificate.md) Objekte in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="e1890-106">The **Count** property retrieves the number of [**Certificate**](certificate.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1890-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1890-107">Syntax</span></span>


```VB
Certificates.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="e1890-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e1890-108">Property value</span></span>

<span data-ttu-id="e1890-109">Die Anzahl der [**Zertifikat**](certificate.md) Objekte in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="e1890-109">The number of [**Certificate**](certificate.md) objects in the collection.</span></span> <span data-ttu-id="e1890-110">Jedes **Zertifikat** Objekt stellt ein einzelnes Zertifikat in der Sammlung dar.</span><span class="sxs-lookup"><span data-stu-id="e1890-110">Each **Certificate** object represents a single certificate in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1890-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1890-111">Remarks</span></span>

<span data-ttu-id="e1890-112">CAPICOM unterstützt nur ein einzelnes Zertifikat für den [*smartcardspeicher*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e1890-112">CAPICOM only supports a single certificate for the [*smart card*](../secgloss/s-gly.md) store.</span></span> <span data-ttu-id="e1890-113">Auch wenn der smartcardspeicher mehr als ein Zertifikat enthält, enthält diese Eigenschaft den Wert 1.</span><span class="sxs-lookup"><span data-stu-id="e1890-113">Even if the smart card store contains more than one certificate, this property will contain 1.</span></span> <span data-ttu-id="e1890-114">Weitere Informationen zum smartcardspeicher finden Sie unter dem **CAPICOM- \_ \_ Smartcard- \_ Benutzer \_ Speicher** Mitglied der " [**CAPICOM \_ Store \_ Location**](capicom-store-location.md) "-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="e1890-114">For more information about the smart card store, see the **CAPICOM\_SMART\_CARD\_USER\_STORE** member of the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1890-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1890-115">Requirements</span></span>



| <span data-ttu-id="e1890-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1890-116">Requirement</span></span> | <span data-ttu-id="e1890-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e1890-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1890-118">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e1890-118">End of client support</span></span><br/> | <span data-ttu-id="e1890-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1890-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e1890-120">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="e1890-120">End of server support</span></span><br/> | <span data-ttu-id="e1890-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1890-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e1890-122">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e1890-122">Redistributable</span></span><br/>       | <span data-ttu-id="e1890-123">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="e1890-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e1890-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e1890-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e1890-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1890-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1890-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1890-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1890-127">**Zertifikate**</span><span class="sxs-lookup"><span data-stu-id="e1890-127">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
