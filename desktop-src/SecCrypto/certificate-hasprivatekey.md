---
description: Bestimmt, ob dem Zertifikat ein privater Schlüssel zugeordnet ist. Die-Methode bestimmt dies, indem Sie überprüft, ob die \_ Eigenschaft Zertifikat Schlüssel \_ Prov \_ Info \_ Prop \_ ID vorhanden ist.
ms.assetid: 80478956-1ed7-4c25-9ae3-d7176649e6d7
title: 'ICertificate2:: HasPrivateKey-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.HasPrivateKey
- ICertificate2.HasPrivateKey
- ICertificate.HasPrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 43110e48a1172977ad979d6ec2d94c5b8e3ffc50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353827"
---
# <a name="icertificate2hasprivatekey-method"></a><span data-ttu-id="fe4bc-104">ICertificate2:: HasPrivateKey-Methode</span><span class="sxs-lookup"><span data-stu-id="fe4bc-104">ICertificate2::HasPrivateKey method</span></span>

<span data-ttu-id="fe4bc-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fe4bc-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="fe4bc-106">Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="fe4bc-106">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="fe4bc-107">Die **HasPrivateKey** -Methode bestimmt, ob dem [*Zertifikat*](../secgloss/c-gly.md) ein [*privater Schlüssel*](../secgloss/p-gly.md) zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fe4bc-107">The **HasPrivateKey** method determines whether the [*certificate*](../secgloss/c-gly.md) has a [*private key*](../secgloss/p-gly.md) associated with it.</span></span> <span data-ttu-id="fe4bc-108">Die-Methode bestimmt dies, indem Sie überprüft, ob die \_ Eigenschaft Zertifikat Schlüssel \_ Prov \_ Info \_ Prop \_ ID vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="fe4bc-108">The method determines this by checking whether the CERT\_KEY\_PROV\_INFO\_PROP\_ID property is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe4bc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe4bc-109">Syntax</span></span>


```VB
Certificate.HasPrivateKey()
```



## <a name="parameters"></a><span data-ttu-id="fe4bc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe4bc-110">Parameters</span></span>

<span data-ttu-id="fe4bc-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="fe4bc-111">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe4bc-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe4bc-112">Requirements</span></span>



| <span data-ttu-id="fe4bc-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe4bc-113">Requirement</span></span> | <span data-ttu-id="fe4bc-114">Wert</span><span class="sxs-lookup"><span data-stu-id="fe4bc-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe4bc-115">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="fe4bc-115">End of client support</span></span><br/> | <span data-ttu-id="fe4bc-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe4bc-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fe4bc-117">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="fe4bc-117">End of server support</span></span><br/> | <span data-ttu-id="fe4bc-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe4bc-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fe4bc-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="fe4bc-119">Redistributable</span></span><br/>       | <span data-ttu-id="fe4bc-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe4bc-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fe4bc-121">DLL</span><span class="sxs-lookup"><span data-stu-id="fe4bc-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="fe4bc-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe4bc-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe4bc-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe4bc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe4bc-124">**PrivateKey. Open**</span><span class="sxs-lookup"><span data-stu-id="fe4bc-124">**PrivateKey.Open**</span></span>](privatekey-open.md)
</dt> <dt>

[<span data-ttu-id="fe4bc-125">Kryptografieobjekte</span><span class="sxs-lookup"><span data-stu-id="fe4bc-125">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="fe4bc-126">**Stellt**</span><span class="sxs-lookup"><span data-stu-id="fe4bc-126">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
