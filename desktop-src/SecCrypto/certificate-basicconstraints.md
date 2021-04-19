---
description: Gibt ein basiceinschränkungs-Objekt zurück, das die grundlegende Einschränkungs Erweiterung des Zertifikats darstellt.
ms.assetid: cc4e566a-5f68-4e28-9397-39f22a71e45b
title: 'ICertificate2:: basiceinschränkungs-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.BasicConstraints
- ICertificate2.BasicConstraints
- ICertificate.BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b511781c29d313715e7714f185dbff7e4b38f86c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360445"
---
# <a name="icertificate2basicconstraints-method"></a><span data-ttu-id="59e81-103">ICertificate2:: basiceinschränkungs-Methode</span><span class="sxs-lookup"><span data-stu-id="59e81-103">ICertificate2::BasicConstraints method</span></span>

<span data-ttu-id="59e81-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="59e81-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="59e81-105">Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="59e81-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="59e81-106">Die **basiceinschränkungs** -Methode gibt ein [**basiceinschränkungs**](basicconstraints.md) -Objekt zurück, das die grundlegende Einschränkungs Erweiterung des Zertifikats darstellt.</span><span class="sxs-lookup"><span data-stu-id="59e81-106">The **BasicConstraints** method returns a [**BasicConstraints**](basicconstraints.md) object that represents the basic constraints extension of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="59e81-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="59e81-107">Syntax</span></span>


```VB
Certificate.BasicConstraints()
```



## <a name="parameters"></a><span data-ttu-id="59e81-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="59e81-108">Parameters</span></span>

<span data-ttu-id="59e81-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="59e81-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59e81-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59e81-110">Return value</span></span>

<span data-ttu-id="59e81-111">Das [**basiceinschränkunsobjekt**](basicconstraints.md) , das die grundlegende Einschränkungs Erweiterung des Zertifikats darstellt.</span><span class="sxs-lookup"><span data-stu-id="59e81-111">The [**BasicConstraints**](basicconstraints.md) object that represents the basic constraints extension of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="59e81-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59e81-112">Requirements</span></span>



| <span data-ttu-id="59e81-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59e81-113">Requirement</span></span> | <span data-ttu-id="59e81-114">Wert</span><span class="sxs-lookup"><span data-stu-id="59e81-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59e81-115">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="59e81-115">End of client support</span></span><br/> | <span data-ttu-id="59e81-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59e81-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="59e81-117">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="59e81-117">End of server support</span></span><br/> | <span data-ttu-id="59e81-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59e81-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="59e81-119">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="59e81-119">Redistributable</span></span><br/>       | <span data-ttu-id="59e81-120">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="59e81-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="59e81-121">DLL</span><span class="sxs-lookup"><span data-stu-id="59e81-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="59e81-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59e81-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
