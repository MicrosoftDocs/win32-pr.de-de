---
description: Die Skip-Methode überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz. Diese Methode ist in Visual Basic-und Skriptsprachen ausgeblendet.
ms.assetid: 7f641354-c3f5-4eb3-ad1c-98abf7694106
title: 'Ienumparticipants:: Skip-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc406a69c126c25b1c554679595868a595b839b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369174"
---
# <a name="ienumparticipantskip-method"></a><span data-ttu-id="960e9-104">Ienumteilnehmer:: Skip-Methode</span><span class="sxs-lookup"><span data-stu-id="960e9-104">IEnumParticipant::Skip method</span></span>

<span data-ttu-id="960e9-105">\[**Skip** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="960e9-105">\[**Skip** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="960e9-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="960e9-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="960e9-107">Die **Skip** -Methode überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="960e9-107">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="960e9-108">Diese Methode ist in Visual Basic-und Skriptsprachen ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="960e9-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="960e9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="960e9-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="960e9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="960e9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="960e9-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="960e9-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="960e9-112">Anzahl der zu überspringenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="960e9-112">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="960e9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="960e9-113">Return value</span></span>

<span data-ttu-id="960e9-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="960e9-114">This method can return one of these values.</span></span>



| <span data-ttu-id="960e9-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="960e9-115">Return code</span></span>                                                                                   | <span data-ttu-id="960e9-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="960e9-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="960e9-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="960e9-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="960e9-118">Die Anzahl übersprungener Elemente war " *celt*".</span><span class="sxs-lookup"><span data-stu-id="960e9-118">Number of elements skipped was *celt*.</span></span><br/>               |
| <dl> <span data-ttu-id="960e9-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="960e9-119"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="960e9-120">Die Anzahl übersprungener Elemente war nicht " *celt*".</span><span class="sxs-lookup"><span data-stu-id="960e9-120">Number of elements skipped was not *celt*.</span></span><br/>           |
| <dl> <span data-ttu-id="960e9-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="960e9-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="960e9-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="960e9-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="960e9-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="960e9-123">Requirements</span></span>



| <span data-ttu-id="960e9-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="960e9-124">Requirement</span></span> | <span data-ttu-id="960e9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="960e9-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="960e9-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="960e9-126">TAPI version</span></span><br/> | <span data-ttu-id="960e9-127">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="960e9-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="960e9-128">Header</span><span class="sxs-lookup"><span data-stu-id="960e9-128">Header</span></span><br/>       | <dl> <span data-ttu-id="960e9-129"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="960e9-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="960e9-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="960e9-130">Library</span></span><br/>      | <dl> <span data-ttu-id="960e9-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="960e9-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="960e9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="960e9-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="960e9-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="960e9-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="960e9-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="960e9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="960e9-135">**Ienumteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="960e9-135">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="960e9-136">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="960e9-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




