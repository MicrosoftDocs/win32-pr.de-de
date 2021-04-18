---
description: Mit der get \_ substreamfromparticipants-Methode kann eine Anwendung ermitteln, welche Substreams einem bestimmten Teilnehmer zugeordnet sind.
ms.assetid: d45cdd1d-13cf-433a-9b19-193d5c0cba11
title: 'Itparticipantsubstreamcontrol:: get_SubStreamFromParticipant-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0eae68cd62c38348e1a576f114a9e93ac52f9cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364493"
---
# <a name="itparticipantsubstreamcontrolget_substreamfromparticipant-method"></a><span data-ttu-id="926c4-103">Itparticipantsubstreamcontrol:: get \_ substreamfromparticipants-Methode</span><span class="sxs-lookup"><span data-stu-id="926c4-103">ITParticipantSubStreamControl::get\_SubStreamFromParticipant method</span></span>

<span data-ttu-id="926c4-104">\[**get \_ Substreamfromteilnehmer** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="926c4-104">\[**get\_SubStreamFromParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="926c4-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="926c4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="926c4-106">Mit der **get \_ substreamfromparticipants** -Methode kann eine Anwendung ermitteln, welche Substreams einem bestimmten Teilnehmer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="926c4-106">The **get\_SubStreamFromParticipant** method allows an application to discover which substreams are associated with a given participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="926c4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="926c4-107">Syntax</span></span>


```C++
HRESULT get_SubStreamFromParticipant(
  [in]  ITParticipant *pParticipant,
  [out] ITSubStream   **ppITSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="926c4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="926c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="926c4-109">*pteilnehmer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="926c4-109">*pParticipant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="926c4-110">Zeiger auf die [**itparticipants**](itparticipant.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="926c4-110">Pointer to [**ITParticipant**](itparticipant.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="926c4-111">*ppitsubstream* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="926c4-111">*ppITSubStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="926c4-112">Zeiger auf ein Array von [**itteilnehmer**](itparticipant.md) -Schnittstellen Zeigern.</span><span class="sxs-lookup"><span data-stu-id="926c4-112">Pointer to array of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="926c4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="926c4-113">Return value</span></span>

<span data-ttu-id="926c4-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="926c4-114">This method can return one of these values.</span></span>



| <span data-ttu-id="926c4-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="926c4-115">Return code</span></span>                                                                                   | <span data-ttu-id="926c4-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="926c4-116">Description</span></span>                                                                  |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="926c4-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="926c4-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="926c4-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="926c4-118">Method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="926c4-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="926c4-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="926c4-120">Der *ppitsubstream* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="926c4-120">The *ppITSubStream* parameter is not a valid pointer.</span></span><br/>             |
| <dl> <span data-ttu-id="926c4-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="926c4-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="926c4-122">Der *pparticipants* -Parameter verweist nicht auf eine gültige Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="926c4-122">The *pParticipant* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="926c4-123"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="926c4-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="926c4-124">Auf die Teilnehmer Informationen des Streams konnte nicht zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="926c4-124">The stream's participant information could not be accessed.</span></span><br/>       |
| <dl> <span data-ttu-id="926c4-125"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="926c4-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="926c4-126">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="926c4-126">Insufficient memory exists to perform the operation.</span></span><br/>              |



 

## <a name="requirements"></a><span data-ttu-id="926c4-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="926c4-127">Requirements</span></span>



| <span data-ttu-id="926c4-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="926c4-128">Requirement</span></span> | <span data-ttu-id="926c4-129">Wert</span><span class="sxs-lookup"><span data-stu-id="926c4-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="926c4-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="926c4-130">TAPI version</span></span><br/> | <span data-ttu-id="926c4-131">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="926c4-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="926c4-132">Header</span><span class="sxs-lookup"><span data-stu-id="926c4-132">Header</span></span><br/>       | <dl> <span data-ttu-id="926c4-133"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="926c4-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="926c4-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="926c4-134">Library</span></span><br/>      | <dl> <span data-ttu-id="926c4-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="926c4-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="926c4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="926c4-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="926c4-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="926c4-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="926c4-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="926c4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="926c4-139">**Itparticipantsubstreamcontrol**</span><span class="sxs-lookup"><span data-stu-id="926c4-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="926c4-140">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="926c4-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="926c4-141">**Itsubstream**</span><span class="sxs-lookup"><span data-stu-id="926c4-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

