---
description: Erstellt eine Zertifikat Überprüfungs Kette für ein Zertifikat und gibt ein CertificateStatus-Objekt zurück, das den Gültigkeits Status des Zertifikats enthält.
ms.assetid: 4463e4ac-60a5-4845-93b3-35d2f83bd86e
title: 'ICertificate2:: IsValid-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IsValid
- ICertificate2.IsValid
- ICertificate.IsValid
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 39fec7c1bd2b369ee512834ed1b58b59871d8ae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369399"
---
# <a name="icertificate2isvalid-method"></a><span data-ttu-id="a9121-103">ICertificate2:: IsValid-Methode</span><span class="sxs-lookup"><span data-stu-id="a9121-103">ICertificate2::IsValid method</span></span>

<span data-ttu-id="a9121-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a9121-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a9121-105">Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="a9121-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a9121-106">Die **IsValid** -Methode erstellt eine Zertifikat Überprüfungs Kette für ein Zertifikat und gibt ein [**CertificateStatus**](certificatestatus.md) -Objekt zurück, das den Gültigkeits Status des Zertifikats enthält.</span><span class="sxs-lookup"><span data-stu-id="a9121-106">The **IsValid** method builds a certificate verification chain for a certificate and returns a [**CertificateStatus**](certificatestatus.md) object that contains the validity status of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9121-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9121-107">Syntax</span></span>


```VB
Certificate.IsValid()
```



## <a name="parameters"></a><span data-ttu-id="a9121-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9121-108">Parameters</span></span>

<span data-ttu-id="a9121-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a9121-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9121-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9121-110">Requirements</span></span>



| <span data-ttu-id="a9121-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9121-111">Requirement</span></span> | <span data-ttu-id="a9121-112">Wert</span><span class="sxs-lookup"><span data-stu-id="a9121-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9121-113">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a9121-113">End of client support</span></span><br/> | <span data-ttu-id="a9121-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9121-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a9121-115">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="a9121-115">End of server support</span></span><br/> | <span data-ttu-id="a9121-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9121-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a9121-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="a9121-117">Redistributable</span></span><br/>       | <span data-ttu-id="a9121-118">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="a9121-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a9121-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a9121-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a9121-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9121-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9121-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9121-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9121-122">Kryptografieobjekte</span><span class="sxs-lookup"><span data-stu-id="a9121-122">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="a9121-123">**Stellt**</span><span class="sxs-lookup"><span data-stu-id="a9121-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
