---
description: Der get- \_ substream erhält einen Zeiger auf ein Array von itsubstream-Schnittstellen, die die am Ereignis beteiligten untergeordneten Datenströme darstellen.
ms.assetid: 0af9097a-2481-4543-bb3d-35ccd352e992
title: 'Itparticipvorgänger Vent:: get_SubStream-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8c2944004af31adfb7256376992506eef59b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372088"
---
# <a name="itparticipanteventget_substream-method"></a><span data-ttu-id="a3640-103">Itparticipvorgänger Vent:: get \_ substream-Methode</span><span class="sxs-lookup"><span data-stu-id="a3640-103">ITParticipantEvent::get\_SubStream method</span></span>

<span data-ttu-id="a3640-104">\[**get \_ Substream** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a3640-104">\[**get\_SubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a3640-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="a3640-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a3640-106">Der **get- \_ substream** erhält einen Zeiger auf ein Array von [**itsubstream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) -Schnittstellen, die die am Ereignis beteiligten untergeordneten Datenströme darstellen.</span><span class="sxs-lookup"><span data-stu-id="a3640-106">The **get\_SubStream** gets a pointer to an array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interfaces representing the substreams involved in the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3640-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3640-107">Syntax</span></span>


```C++
HRESULT get_SubStream(
  [out] ITSubStream **ppSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="a3640-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3640-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3640-109">*ppsubstream* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a3640-109">*ppSubStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3640-110">Zeiger auf ein Array von [**itsubstream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) -Zeigern.</span><span class="sxs-lookup"><span data-stu-id="a3640-110">Pointer to array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3640-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3640-111">Return value</span></span>

<span data-ttu-id="a3640-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a3640-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a3640-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a3640-113">Value</span></span>                                                                                           | <span data-ttu-id="a3640-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a3640-114">Meaning</span></span>                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a3640-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a3640-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="a3640-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a3640-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a3640-117"><dt>**TAPI \_ E \_ noItems**</dt></span><span class="sxs-lookup"><span data-stu-id="a3640-117"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="a3640-118">Dem Ereignis sind keine Substreams zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a3640-118">There are no substreams associated with the event.</span></span><br/>   |
| <dl> <span data-ttu-id="a3640-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="a3640-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="a3640-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a3640-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a3640-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="a3640-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="a3640-122">Der *ppsubstream* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="a3640-122">The *ppSubStream* parameter is not a valid pointer.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="a3640-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3640-123">Requirements</span></span>



| <span data-ttu-id="a3640-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3640-124">Requirement</span></span> | <span data-ttu-id="a3640-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a3640-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3640-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="a3640-126">TAPI version</span></span><br/> | <span data-ttu-id="a3640-127">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="a3640-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a3640-128">Header</span><span class="sxs-lookup"><span data-stu-id="a3640-128">Header</span></span><br/>       | <dl> <span data-ttu-id="a3640-129"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a3640-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="a3640-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a3640-130">Library</span></span><br/>      | <dl> <span data-ttu-id="a3640-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3640-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a3640-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a3640-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="a3640-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3640-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a3640-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3640-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3640-135">**Itparticipvorgänger Vent**</span><span class="sxs-lookup"><span data-stu-id="a3640-135">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="a3640-136">**Itsubstream**</span><span class="sxs-lookup"><span data-stu-id="a3640-136">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

