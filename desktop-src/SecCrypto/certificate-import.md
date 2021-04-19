---
description: Importiert ein zuvor codiertes Zertifikat aus einer Zeichenfolge in das Zertifikat Objekt.
ms.assetid: 8515e034-08aa-4575-9b96-34cdee3ccba8
title: 'ICertificate2:: Import-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Import
- ICertificate2.Import
- ICertificate.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ea639f1cd89b673ecf8da77302e3d812894a202b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360357"
---
# <a name="icertificate2import-method"></a><span data-ttu-id="0ef8f-103">ICertificate2:: Import-Methode</span><span class="sxs-lookup"><span data-stu-id="0ef8f-103">ICertificate2::Import method</span></span>

<span data-ttu-id="0ef8f-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0ef8f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0ef8f-105">Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="0ef8f-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0ef8f-106">Die **Import** -Methode importiert ein zuvor codiertes Zertifikat aus einer Zeichenfolge in das [**Zertifikat**](certificate.md) Objekt.</span><span class="sxs-lookup"><span data-stu-id="0ef8f-106">The **Import** method imports a previously encoded certificate from a string into the [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="0ef8f-107">Durch Aufrufen dieser Methode wird der [*Zustand*](../secgloss/s-gly.md) dieses Objekts zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="0ef8f-107">Calling this method resets the [*state*](../secgloss/s-gly.md) of this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef8f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ef8f-108">Syntax</span></span>


```VB
Certificate.Import( _
  ByVal EncodedCertificate _
)
```



## <a name="parameters"></a><span data-ttu-id="0ef8f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ef8f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ef8f-110">*Encodcertificate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ef8f-110">*EncodedCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef8f-111">Eine Zeichenfolge, die die zu importierenden codierten Zertifikatsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="0ef8f-111">A string that contains the encoded certificate data to be imported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ef8f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ef8f-112">Return value</span></span>

<span data-ttu-id="0ef8f-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0ef8f-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ef8f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ef8f-114">Requirements</span></span>



| <span data-ttu-id="0ef8f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ef8f-115">Requirement</span></span> | <span data-ttu-id="0ef8f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0ef8f-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef8f-117">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0ef8f-117">End of client support</span></span><br/> | <span data-ttu-id="0ef8f-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ef8f-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0ef8f-119">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="0ef8f-119">End of server support</span></span><br/> | <span data-ttu-id="0ef8f-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ef8f-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0ef8f-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="0ef8f-121">Redistributable</span></span><br/>       | <span data-ttu-id="0ef8f-122">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="0ef8f-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0ef8f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0ef8f-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0ef8f-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ef8f-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ef8f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ef8f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef8f-126">Kryptografieobjekte</span><span class="sxs-lookup"><span data-stu-id="0ef8f-126">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="0ef8f-127">**Stellt**</span><span class="sxs-lookup"><span data-stu-id="0ef8f-127">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
