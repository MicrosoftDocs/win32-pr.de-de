---
description: Gibt eine Zeichenfolge zurück, die zusätzliche Fehlerinformationen zum indizierten Eintrag enthält.
ms.assetid: 4f0d5289-c414-4e2b-b612-be8ce1d98b12
title: 'IChain2:: ExtendedErrorInfo-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ExtendedErrorInfo
- IChain2.ExtendedErrorInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f8a7840d0f54ea7e93ad9998d5e8772a2ae411f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371617"
---
# <a name="ichain2extendederrorinfo-method"></a><span data-ttu-id="269e3-103">IChain2:: ExtendedErrorInfo-Methode</span><span class="sxs-lookup"><span data-stu-id="269e3-103">IChain2::ExtendedErrorInfo method</span></span>

<span data-ttu-id="269e3-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="269e3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="269e3-105">Verwenden Sie stattdessen die [**X509Chain-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="269e3-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="269e3-106">Die **ExtendedErrorInfo** -Methode gibt eine Zeichenfolge zurück, die zusätzliche Fehlerinformationen zum indizierten Eintrag enthält.</span><span class="sxs-lookup"><span data-stu-id="269e3-106">The **ExtendedErrorInfo** method returns a string that contains additional error information about the indexed entry.</span></span>

<span data-ttu-id="269e3-107">Diese Methode wird in CAPICOM 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="269e3-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="269e3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="269e3-108">Syntax</span></span>


```VB
Chain.ExtendedErrorInfo( _
  [ ByVal Index ] _
)
```



## <a name="parameters"></a><span data-ttu-id="269e3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="269e3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="269e3-110">*Index* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="269e3-110">*Index* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="269e3-111">Ein **Long** -Wert, der den Index des Eintrags darstellt.</span><span class="sxs-lookup"><span data-stu-id="269e3-111">A **Long** representing the index of the entry.</span></span> <span data-ttu-id="269e3-112">Der Standardwert ist 1, wodurch Fehlerinformationen für das Endzertifikat in der Kette zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="269e3-112">The default value is 1, which returns error information for the end certificate in the chain.</span></span> <span data-ttu-id="269e3-113">" **Zertifikate. count** " gibt Informationen zum Stamm Zertifikat der Kette zurück.</span><span class="sxs-lookup"><span data-stu-id="269e3-113">**Certificates.Count** returns information about the root certificate of the chain.</span></span> <span data-ttu-id="269e3-114">0 gibt erweiterte Fehlerinformationen für die gesamte Kette zurück.</span><span class="sxs-lookup"><span data-stu-id="269e3-114">0 returns extended error information for the entire chain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="269e3-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="269e3-115">Return value</span></span>

<span data-ttu-id="269e3-116">Eine Zeichenfolge, die die erweiterten Fehlerinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="269e3-116">A string that contains the extended error information.</span></span>

## <a name="requirements"></a><span data-ttu-id="269e3-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="269e3-117">Requirements</span></span>



| <span data-ttu-id="269e3-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="269e3-118">Requirement</span></span> | <span data-ttu-id="269e3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="269e3-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="269e3-120">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="269e3-120">End of client support</span></span><br/> | <span data-ttu-id="269e3-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="269e3-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="269e3-122">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="269e3-122">End of server support</span></span><br/> | <span data-ttu-id="269e3-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="269e3-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="269e3-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="269e3-124">Redistributable</span></span><br/>       | <span data-ttu-id="269e3-125">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="269e3-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="269e3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="269e3-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="269e3-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="269e3-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="269e3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="269e3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="269e3-129">**Ketten**</span><span class="sxs-lookup"><span data-stu-id="269e3-129">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
