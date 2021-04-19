---
description: Gibt ein extendedkeyusage-Objekt zurück, das die gültigen Verwendungen des Zertifikats angibt.
ms.assetid: e974e9e2-1011-48b7-9ebc-e754e4990286
title: 'ICertificate2:: extendedkeyusage-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ExtendedKeyUsage
- ICertificate2.ExtendedKeyUsage
- ICertificate.ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6f349b7267d58a9376b9295e3ffd5013954a0872
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354167"
---
# <a name="icertificate2extendedkeyusage-method"></a><span data-ttu-id="bf0a2-103">ICertificate2:: extendedkeyusage-Methode</span><span class="sxs-lookup"><span data-stu-id="bf0a2-103">ICertificate2::ExtendedKeyUsage method</span></span>

<span data-ttu-id="bf0a2-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bf0a2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="bf0a2-105">Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="bf0a2-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="bf0a2-106">Die **extendedkeyusage** -Methode gibt ein [**extendedkeyusage**](extendedkeyusage.md) -Objekt zurück, das die gültigen Verwendungen des Zertifikats angibt.</span><span class="sxs-lookup"><span data-stu-id="bf0a2-106">The **ExtendedKeyUsage** method returns an [**ExtendedKeyUsage**](extendedkeyusage.md) object that indicates the valid uses of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf0a2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf0a2-107">Syntax</span></span>


```VB
Certificate.ExtendedKeyUsage()
```



## <a name="parameters"></a><span data-ttu-id="bf0a2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf0a2-108">Parameters</span></span>

<span data-ttu-id="bf0a2-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="bf0a2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bf0a2-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bf0a2-110">Return value</span></span>

<span data-ttu-id="bf0a2-111">Das [**extendedkeyusage**](extendedkeyusage.md) -Objekt, das dem Zertifikat zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bf0a2-111">The [**ExtendedKeyUsage**](extendedkeyusage.md) object that is associated with the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf0a2-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf0a2-112">Requirements</span></span>



| <span data-ttu-id="bf0a2-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf0a2-113">Requirement</span></span> | <span data-ttu-id="bf0a2-114">Wert</span><span class="sxs-lookup"><span data-stu-id="bf0a2-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf0a2-115">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="bf0a2-115">End of client support</span></span><br/> | <span data-ttu-id="bf0a2-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf0a2-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bf0a2-117">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="bf0a2-117">End of server support</span></span><br/> | <span data-ttu-id="bf0a2-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf0a2-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bf0a2-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="bf0a2-119">Redistributable</span></span><br/>       | <span data-ttu-id="bf0a2-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="bf0a2-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bf0a2-121">DLL</span><span class="sxs-lookup"><span data-stu-id="bf0a2-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="bf0a2-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf0a2-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf0a2-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf0a2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf0a2-124">Kryptografieobjekte</span><span class="sxs-lookup"><span data-stu-id="bf0a2-124">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="bf0a2-125">**Stellt**</span><span class="sxs-lookup"><span data-stu-id="bf0a2-125">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
