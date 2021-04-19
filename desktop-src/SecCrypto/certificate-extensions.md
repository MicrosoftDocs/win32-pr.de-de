---
description: Gibt eine Auflistung der Erweiterungen zurück, die dem Zertifikat zugeordnet sind.
ms.assetid: 07793061-6f94-4467-bb01-aa65db657658
title: 'ICertificate2:: Extensions-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Extensions
- ICertificate2.Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cc96dee9c33bb3f76e1fb17acb2000f9740d1b5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355948"
---
# <a name="icertificate2extensions-method"></a><span data-ttu-id="c36a1-103">ICertificate2:: Extensions-Methode</span><span class="sxs-lookup"><span data-stu-id="c36a1-103">ICertificate2::Extensions method</span></span>

<span data-ttu-id="c36a1-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c36a1-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c36a1-105">Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="c36a1-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c36a1-106">Die **Extensions** -Methode gibt eine Auflistung der Erweiterungen zurück, die dem Zertifikat zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c36a1-106">The **Extensions** method returns a collection of the extensions associated with the certificate.</span></span> <span data-ttu-id="c36a1-107">Diese Methode wird in CAPICOM 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c36a1-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="c36a1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c36a1-108">Syntax</span></span>


```VB
Certificate.Extensions()
```



## <a name="parameters"></a><span data-ttu-id="c36a1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c36a1-109">Parameters</span></span>

<span data-ttu-id="c36a1-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c36a1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c36a1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c36a1-111">Return value</span></span>

<span data-ttu-id="c36a1-112">Ein [**Erweiterungs**](extensions.md) Objekt, das alle dem Zertifikat zugeordneten Erweiterungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="c36a1-112">An [**Extensions**](extensions.md) object that represents all of the extensions associated with the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="c36a1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c36a1-113">Requirements</span></span>



| <span data-ttu-id="c36a1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c36a1-114">Requirement</span></span> | <span data-ttu-id="c36a1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c36a1-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c36a1-116">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c36a1-116">End of client support</span></span><br/> | <span data-ttu-id="c36a1-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c36a1-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c36a1-118">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c36a1-118">End of server support</span></span><br/> | <span data-ttu-id="c36a1-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c36a1-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c36a1-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c36a1-120">Redistributable</span></span><br/>       | <span data-ttu-id="c36a1-121">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="c36a1-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c36a1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c36a1-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c36a1-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c36a1-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
