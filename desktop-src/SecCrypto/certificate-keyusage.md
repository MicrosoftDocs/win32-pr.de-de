---
description: Gibt ein KeyUsage-Objekt zurück, das die gültige Schlüssel Verwendung des Zertifikats angibt.
ms.assetid: e4590e95-ffa2-4953-bfc1-4d7c70271029
title: 'ICertificate2:: KeyUsage-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.KeyUsage
- ICertificate2.KeyUsage
- ICertificate.KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85fe008880d9613586d38dba7afaca39bb29f72f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372733"
---
# <a name="icertificate2keyusage-method"></a><span data-ttu-id="af90d-103">ICertificate2:: KeyUsage-Methode</span><span class="sxs-lookup"><span data-stu-id="af90d-103">ICertificate2::KeyUsage method</span></span>

<span data-ttu-id="af90d-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="af90d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="af90d-105">Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="af90d-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="af90d-106">Die **KeyUsage** -Methode gibt ein [**KeyUsage**](keyusage.md) -Objekt zurück, das die gültige Schlüssel Verwendung des Zertifikats angibt.</span><span class="sxs-lookup"><span data-stu-id="af90d-106">The **KeyUsage** method returns a [**KeyUsage**](keyusage.md) object that indicates the valid key usage of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="af90d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="af90d-107">Syntax</span></span>


```VB
Certificate.KeyUsage()
```



## <a name="parameters"></a><span data-ttu-id="af90d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="af90d-108">Parameters</span></span>

<span data-ttu-id="af90d-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="af90d-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="af90d-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af90d-110">Requirements</span></span>



| <span data-ttu-id="af90d-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af90d-111">Requirement</span></span> | <span data-ttu-id="af90d-112">Wert</span><span class="sxs-lookup"><span data-stu-id="af90d-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af90d-113">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="af90d-113">End of client support</span></span><br/> | <span data-ttu-id="af90d-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af90d-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="af90d-115">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="af90d-115">End of server support</span></span><br/> | <span data-ttu-id="af90d-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af90d-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="af90d-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="af90d-117">Redistributable</span></span><br/>       | <span data-ttu-id="af90d-118">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="af90d-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="af90d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="af90d-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="af90d-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af90d-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af90d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af90d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af90d-122">Kryptografieobjekte</span><span class="sxs-lookup"><span data-stu-id="af90d-122">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="af90d-123">**Stellt**</span><span class="sxs-lookup"><span data-stu-id="af90d-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
