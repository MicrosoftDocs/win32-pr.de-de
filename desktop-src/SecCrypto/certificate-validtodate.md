---
description: Ruft das Enddatum für die Gültigkeit des Zertifikats ab.
ms.assetid: 25e76b25-9a18-439c-acb8-e0af97b6fcd5
title: Certificate. validtodate (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ValidToDate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 08f6c0748c38ec31085c937eda37a413a3644f13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372044"
---
# <a name="certificatevalidtodate-property"></a><span data-ttu-id="27bf8-103">Certificate. validtodate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="27bf8-103">Certificate.ValidToDate property</span></span>

<span data-ttu-id="27bf8-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="27bf8-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="27bf8-105">Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="27bf8-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="27bf8-106">Die **validtodate** -Eigenschaft ruft das Enddatum für die Gültigkeit des Zertifikats ab.</span><span class="sxs-lookup"><span data-stu-id="27bf8-106">The **ValidToDate** property retrieves the ending date for the validity of the certificate.</span></span>

<span data-ttu-id="27bf8-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="27bf8-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="27bf8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="27bf8-108">Syntax</span></span>


```VB
Certificate.ValidToDate As Date
```



## <a name="property-value"></a><span data-ttu-id="27bf8-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="27bf8-109">Property value</span></span>

<span data-ttu-id="27bf8-110">Ein Datum, das das Enddatum für die Gültigkeit des Zertifikats angibt.</span><span class="sxs-lookup"><span data-stu-id="27bf8-110">A date that indicates the ending date for the validity of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="27bf8-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27bf8-111">Requirements</span></span>



| <span data-ttu-id="27bf8-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27bf8-112">Requirement</span></span> | <span data-ttu-id="27bf8-113">Wert</span><span class="sxs-lookup"><span data-stu-id="27bf8-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27bf8-114">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="27bf8-114">End of client support</span></span><br/> | <span data-ttu-id="27bf8-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27bf8-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="27bf8-116">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="27bf8-116">End of server support</span></span><br/> | <span data-ttu-id="27bf8-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27bf8-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="27bf8-118">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="27bf8-118">Redistributable</span></span><br/>       | <span data-ttu-id="27bf8-119">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="27bf8-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="27bf8-120">DLL</span><span class="sxs-lookup"><span data-stu-id="27bf8-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="27bf8-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27bf8-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27bf8-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27bf8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27bf8-123">**Stellt**</span><span class="sxs-lookup"><span data-stu-id="27bf8-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
