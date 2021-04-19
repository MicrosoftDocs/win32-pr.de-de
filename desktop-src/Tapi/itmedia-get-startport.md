---
description: Mit der get \_ startport-Methode wird der 16-Bit-Portwert für den ersten Port abgerufen.
ms.assetid: 203b51ea-8e0c-47d2-b267-36a0bf3bff72
title: 'ITmedia:: get_StartPort-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c5cf50f4a8beb0a1694bd1ceaf000620c69b69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353826"
---
# <a name="itmediaget_startport-method"></a><span data-ttu-id="63e6d-103">ITmedia:: get \_ startport-Methode</span><span class="sxs-lookup"><span data-stu-id="63e6d-103">ITMedia::get\_StartPort method</span></span>

<span data-ttu-id="63e6d-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="63e6d-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="63e6d-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="63e6d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="63e6d-106">Mit der **get \_ startport** -Methode wird der 16-Bit-Portwert für den ersten Port abgerufen.</span><span class="sxs-lookup"><span data-stu-id="63e6d-106">The **get\_StartPort** method gets the 16-bit port value for the first port.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e6d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="63e6d-107">Syntax</span></span>


```C++
HRESULT get_StartPort(
  [out] LONG *pStartPort
);
```



## <a name="parameters"></a><span data-ttu-id="63e6d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="63e6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63e6d-109">*pstartport* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="63e6d-109">*pStartPort* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63e6d-110">Der Wert des ersten Ports.</span><span class="sxs-lookup"><span data-stu-id="63e6d-110">Value of the first port.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63e6d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63e6d-111">Return value</span></span>

<span data-ttu-id="63e6d-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="63e6d-112">This method can return one of these values.</span></span>



| <span data-ttu-id="63e6d-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="63e6d-113">Return code</span></span>                                                                                   | <span data-ttu-id="63e6d-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63e6d-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="63e6d-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="63e6d-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="63e6d-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="63e6d-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="63e6d-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="63e6d-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="63e6d-118">Der *pstartport* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="63e6d-118">The *pStartPort* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="63e6d-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="63e6d-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="63e6d-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="63e6d-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="63e6d-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="63e6d-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="63e6d-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="63e6d-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="63e6d-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="63e6d-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="63e6d-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="63e6d-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="63e6d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63e6d-125">Requirements</span></span>



| <span data-ttu-id="63e6d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63e6d-126">Requirement</span></span> | <span data-ttu-id="63e6d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="63e6d-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63e6d-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="63e6d-128">TAPI version</span></span><br/> | <span data-ttu-id="63e6d-129">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="63e6d-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="63e6d-130">Header</span><span class="sxs-lookup"><span data-stu-id="63e6d-130">Header</span></span><br/>       | <dl> <span data-ttu-id="63e6d-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="63e6d-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="63e6d-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="63e6d-132">Library</span></span><br/>      | <dl> <span data-ttu-id="63e6d-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63e6d-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="63e6d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="63e6d-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="63e6d-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63e6d-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63e6d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63e6d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e6d-137">**ITmedia**</span><span class="sxs-lookup"><span data-stu-id="63e6d-137">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




