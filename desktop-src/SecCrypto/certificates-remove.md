---
description: Entfernt ein einzelnes Zertifikat Objekt aus der Auflistung.
ms.assetid: dff82825-1a7d-4c1a-94e2-7f9d1281ecf2
title: 'ICertificates2:: Remove-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Remove
- ICertificates2.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6a2f9336a420f1d014e178f67cae02cf85f0fd44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359748"
---
# <a name="icertificates2remove-method"></a><span data-ttu-id="85357-103">ICertificates2:: Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="85357-103">ICertificates2::Remove method</span></span>

<span data-ttu-id="85357-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="85357-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="85357-105">Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="85357-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="85357-106">Die **Remove** -Methode entfernt ein einzelnes [**Zertifikat**](certificate.md) Objekt aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="85357-106">The **Remove** method removes a single [**Certificate**](certificate.md) object from the collection.</span></span> <span data-ttu-id="85357-107">Diese Methode wurde in CAPICOM 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="85357-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="85357-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="85357-108">Syntax</span></span>


```VB
Certificates.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="85357-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="85357-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85357-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85357-110">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85357-111">Der Indexwert für das zu entfernende [**Zertifikat**](certificate.md) Objekt.</span><span class="sxs-lookup"><span data-stu-id="85357-111">Index value for the [**Certificate**](certificate.md) object to be removed.</span></span> <span data-ttu-id="85357-112">Dieser Parameter kann einen der folgenden möglichen Typen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="85357-112">This parameter can be one of the following possible types.</span></span>



| <span data-ttu-id="85357-113">type</span><span class="sxs-lookup"><span data-stu-id="85357-113">Type</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="85357-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="85357-114">Meaning</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Long"></span><span id="long"></span><span id="LONG"></span><dl> <span data-ttu-id="85357-115"><dt>\* \* \* \* Long \* \*</dt> \* \* <dt></dt></span><span class="sxs-lookup"><span data-stu-id="85357-115"><dt>\*\*\*\*Long\*\*\*\*</dt> <dt></dt></span></span> </dl>                                                | <span data-ttu-id="85357-116">Das [**Zertifikat**](certificate.md) Objekt am angegebenen Index in die Auflistung wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="85357-116">The [**Certificate**](certificate.md) object at the specified index into the collection is removed.</span></span><br/>                                                                                                          |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <span data-ttu-id="85357-117"><dt>\* \* \* \* Zeichenfolge \* \*</dt> \* \* <dt></dt></span><span class="sxs-lookup"><span data-stu-id="85357-117"><dt>\*\*\*\*String\*\*\*\*</dt> <dt></dt></span></span> </dl>                                        | <span data-ttu-id="85357-118">Das erste [**Zertifikat**](certificate.md) Objekt in der Auflistung, das mit dem in der angegebenen Zeichenfolge enthaltenen [*SHA-1-*](../secgloss/s-gly.md) Fingerabdruck übereinstimmt, wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="85357-118">The first [**Certificate**](certificate.md) object in the collection that matches the [*SHA-1*](../secgloss/s-gly.md) thumbprint contained in the specified string is removed.</span></span><br/> |
| <span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span><dl> <span data-ttu-id="85357-119"><dt>**[**Zertifikat**](certificate.md)**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="85357-119"><dt>**[**Certificate**](certificate.md)**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="85357-120">Das erste [**Zertifikat**](certificate.md) Objekt in der Auflistung, das mit dem angegebenen **Zertifikat** Objekt übereinstimmt, wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="85357-120">The first [**Certificate**](certificate.md) object in the collection that matches the specified **Certificate** object is removed.</span></span><br/>                                                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85357-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85357-121">Return value</span></span>

<span data-ttu-id="85357-122">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="85357-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="85357-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85357-123">Requirements</span></span>



| <span data-ttu-id="85357-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85357-124">Requirement</span></span> | <span data-ttu-id="85357-125">Wert</span><span class="sxs-lookup"><span data-stu-id="85357-125">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85357-126">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="85357-126">End of client support</span></span><br/> | <span data-ttu-id="85357-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85357-127">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="85357-128">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="85357-128">End of server support</span></span><br/> | <span data-ttu-id="85357-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85357-129">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="85357-130">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="85357-130">Redistributable</span></span><br/>       | <span data-ttu-id="85357-131">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="85357-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="85357-132">DLL</span><span class="sxs-lookup"><span data-stu-id="85357-132">DLL</span></span><br/>                   | <dl> <span data-ttu-id="85357-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85357-133"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
