---
description: Die getnumoffunktionalitäten-Methode ruft die Anzahl der Funktionen ab, die dem aktuellen Format zugeordnet sind.
ms.assetid: 26e51c0d-c1cb-410f-ab19-eb884afa8431
title: 'Itformatcontrol:: getnumoffunktionalitäten-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29153f5ee9ce8c5e12b93a1d219905c40f80418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367661"
---
# <a name="itformatcontrolgetnumberofcapabilities-method"></a><span data-ttu-id="8bd65-103">Itformatcontrol:: getnumoffunktionalitäten-Methode</span><span class="sxs-lookup"><span data-stu-id="8bd65-103">ITFormatControl::GetNumberOfCapabilities method</span></span>

<span data-ttu-id="8bd65-104">\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8bd65-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8bd65-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="8bd65-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8bd65-106">Die **getnumoffunktionalitäten** -Methode ruft die Anzahl der Funktionen ab, die dem aktuellen Format zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8bd65-106">The **GetNumberOfCapabilities** method retrieves the number of capabilities associated with the current format.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bd65-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bd65-107">Syntax</span></span>


```C++
HRESULT GetNumberOfCapabilities(
  [out] DWORD *pdwCount
);
```



## <a name="parameters"></a><span data-ttu-id="8bd65-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bd65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bd65-109">*pdwCount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8bd65-109">*pdwCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bd65-110">Anzahl der Funktionen.</span><span class="sxs-lookup"><span data-stu-id="8bd65-110">Count of the capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bd65-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8bd65-111">Return value</span></span>

<span data-ttu-id="8bd65-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8bd65-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8bd65-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8bd65-113">Return code</span></span>                                                                                   | <span data-ttu-id="8bd65-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8bd65-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8bd65-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8bd65-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8bd65-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8bd65-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8bd65-117"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="8bd65-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8bd65-118">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8bd65-118">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8bd65-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8bd65-119">Requirements</span></span>



| <span data-ttu-id="8bd65-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8bd65-120">Requirement</span></span> | <span data-ttu-id="8bd65-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8bd65-121">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8bd65-122">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="8bd65-122">TAPI version</span></span><br/> | <span data-ttu-id="8bd65-123">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="8bd65-123">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="8bd65-124">Header</span><span class="sxs-lookup"><span data-stu-id="8bd65-124">Header</span></span><br/>       | <dl> <span data-ttu-id="8bd65-125"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bd65-125"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8bd65-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8bd65-126">Library</span></span><br/>      | <dl> <span data-ttu-id="8bd65-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bd65-127"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="8bd65-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8bd65-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="8bd65-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bd65-129"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bd65-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bd65-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bd65-131">**Itformatcontrol**</span><span class="sxs-lookup"><span data-stu-id="8bd65-131">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




