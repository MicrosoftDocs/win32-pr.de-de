---
description: Die Skip-Methode überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz.
ms.assetid: e4d9c95d-1b68-4af6-beb2-2014074e5089
title: 'Ienumtime:: Skip-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebd157afc51f52a8453c38f8a14702476c46eb9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370237"
---
# <a name="ienumtimeskip-method"></a><span data-ttu-id="e3c26-103">Ienumtime:: Skip-Methode</span><span class="sxs-lookup"><span data-stu-id="e3c26-103">IEnumTime::Skip method</span></span>

<span data-ttu-id="e3c26-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e3c26-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e3c26-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="e3c26-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e3c26-106">Die **Skip** -Methode überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="e3c26-106">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3c26-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3c26-107">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="e3c26-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3c26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3c26-109">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3c26-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3c26-110">Anzahl der zu überspringenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="e3c26-110">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3c26-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3c26-111">Return value</span></span>

<span data-ttu-id="e3c26-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e3c26-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e3c26-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e3c26-113">Return code</span></span>                                                                             | <span data-ttu-id="e3c26-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3c26-114">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="e3c26-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e3c26-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="e3c26-116">Die Anzahl übersprungener Elemente war " *celt*".</span><span class="sxs-lookup"><span data-stu-id="e3c26-116">Number of elements skipped was *celt*.</span></span><br/>     |
| <dl> <span data-ttu-id="e3c26-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e3c26-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="e3c26-118">Die Anzahl übersprungener Elemente war nicht " *celt*".</span><span class="sxs-lookup"><span data-stu-id="e3c26-118">Number of elements skipped was not *celt*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e3c26-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3c26-119">Requirements</span></span>



| <span data-ttu-id="e3c26-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3c26-120">Requirement</span></span> | <span data-ttu-id="e3c26-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e3c26-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c26-122">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="e3c26-122">TAPI version</span></span><br/> | <span data-ttu-id="e3c26-123">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e3c26-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e3c26-124">Header</span><span class="sxs-lookup"><span data-stu-id="e3c26-124">Header</span></span><br/>       | <dl> <span data-ttu-id="e3c26-125"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3c26-125"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e3c26-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e3c26-126">Library</span></span><br/>      | <dl> <span data-ttu-id="e3c26-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3c26-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e3c26-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e3c26-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="e3c26-129"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3c26-129"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3c26-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3c26-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3c26-131">**Ienumtime**</span><span class="sxs-lookup"><span data-stu-id="e3c26-131">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




