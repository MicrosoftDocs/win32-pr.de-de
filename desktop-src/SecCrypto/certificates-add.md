---
description: Fügt der Auflistung ein Zertifikat Objekt hinzu.
ms.assetid: 0973018d-1e83-41b4-a250-7dd5be2fb664
title: 'ICertificates2:: Add-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Add
- ICertificates2.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d56120c6f584e828c3aadca037d75263d5350f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354681"
---
# <a name="icertificates2add-method"></a><span data-ttu-id="6ab22-103">ICertificates2:: Add-Methode</span><span class="sxs-lookup"><span data-stu-id="6ab22-103">ICertificates2::Add method</span></span>

<span data-ttu-id="6ab22-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6ab22-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6ab22-105">Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="6ab22-105">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6ab22-106">Mit der **Add** -Methode wird der Auflistung ein [**Zertifikat**](certificate.md) Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6ab22-106">The **Add** method adds a [**Certificate**](certificate.md) object to the collection.</span></span> <span data-ttu-id="6ab22-107">Diese Methode wird in CAPICOM 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6ab22-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ab22-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ab22-108">Syntax</span></span>


```VB
Certificates.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="6ab22-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ab22-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ab22-110">*Zertifikat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ab22-110">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab22-111">Das [**Zertifikat**](certificate.md) Objekt, das der Auflistung hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6ab22-111">The [**Certificate**](certificate.md) object to be added to the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ab22-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ab22-112">Return value</span></span>

<span data-ttu-id="6ab22-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6ab22-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ab22-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ab22-114">Requirements</span></span>



| <span data-ttu-id="6ab22-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ab22-115">Requirement</span></span> | <span data-ttu-id="6ab22-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6ab22-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab22-117">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6ab22-117">End of client support</span></span><br/> | <span data-ttu-id="6ab22-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ab22-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6ab22-119">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6ab22-119">End of server support</span></span><br/> | <span data-ttu-id="6ab22-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ab22-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6ab22-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="6ab22-121">Redistributable</span></span><br/>       | <span data-ttu-id="6ab22-122">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="6ab22-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6ab22-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6ab22-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6ab22-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ab22-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
