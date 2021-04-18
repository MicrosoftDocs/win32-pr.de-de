---
description: Mit der get \_ participantfromsubstream-Methode kann eine Anwendung ermitteln, welche Teilnehmer mit einem bestimmten substream verknüpft sind.
ms.assetid: 0e42b4f0-d5b6-4b33-b7e5-dc525524ece7
title: 'Itparticipantsubstreamcontrol:: get_ParticipantFromSubStream-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a507665e7f81339ce10961d69e08e76f60bb2be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352031"
---
# <a name="itparticipantsubstreamcontrolget_participantfromsubstream-method"></a><span data-ttu-id="ef222-103">Itparticipantsubstreamcontrol:: get \_ participantfromsubstream-Methode</span><span class="sxs-lookup"><span data-stu-id="ef222-103">ITParticipantSubStreamControl::get\_ParticipantFromSubStream method</span></span>

<span data-ttu-id="ef222-104">\[**get \_ "Participantfromsubstream** " ist für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ef222-104">\[**get\_ParticipantFromSubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ef222-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="ef222-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ef222-106">Mit der **get \_ participantfromsubstream** -Methode kann eine Anwendung ermitteln, welche Teilnehmer mit einem bestimmten substream verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="ef222-106">The **get\_ParticipantFromSubStream** method allows an application to discover which participants are associated with a given substream.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef222-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef222-107">Syntax</span></span>


```C++
HRESULT get_ParticipantFromSubStream(
  [in]  ITSubStream   *pITSubStream,
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a><span data-ttu-id="ef222-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef222-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef222-109">*pitsubstream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef222-109">*pITSubStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef222-110">Zeiger auf die [**itsubstream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ef222-110">Pointer to [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="ef222-111">*ppteilnehmer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ef222-111">*ppParticipant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef222-112">Zeiger auf ein Array von [**itteilnehmer**](itparticipant.md) -Schnittstellen Zeigern.</span><span class="sxs-lookup"><span data-stu-id="ef222-112">Pointer to array of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef222-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef222-113">Return value</span></span>

<span data-ttu-id="ef222-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ef222-114">This method can return one of these values.</span></span>



| <span data-ttu-id="ef222-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ef222-115">Return code</span></span>                                                                                     | <span data-ttu-id="ef222-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef222-116">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef222-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ef222-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="ef222-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ef222-118">Method succeeded.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="ef222-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="ef222-119"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="ef222-120">Der Parameter " *pitsubstream* " oder " *ppparticipants* " ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="ef222-120">The *pITSubStream* or *ppParticipant* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="ef222-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ef222-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>    | <span data-ttu-id="ef222-122">Der Parameter " *pitsubstream* " verweist nicht auf eine gültige Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ef222-122">The *pITSubStream* parameter does not point to valid interface.</span></span><br/>         |
| <dl> <span data-ttu-id="ef222-123"><dt>**TAPI \_ E \_ noItems**</dt></span><span class="sxs-lookup"><span data-stu-id="ef222-123"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="ef222-124">Dem substream sind keine Teilnehmer zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ef222-124">There are no participants associated with the substream.</span></span><br/>                |
| <dl> <span data-ttu-id="ef222-125"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="ef222-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="ef222-126">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ef222-126">Insufficient memory exists to perform the operation.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="ef222-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef222-127">Requirements</span></span>



| <span data-ttu-id="ef222-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef222-128">Requirement</span></span> | <span data-ttu-id="ef222-129">Wert</span><span class="sxs-lookup"><span data-stu-id="ef222-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef222-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="ef222-130">TAPI version</span></span><br/> | <span data-ttu-id="ef222-131">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ef222-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ef222-132">Header</span><span class="sxs-lookup"><span data-stu-id="ef222-132">Header</span></span><br/>       | <dl> <span data-ttu-id="ef222-133"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ef222-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="ef222-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ef222-134">Library</span></span><br/>      | <dl> <span data-ttu-id="ef222-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef222-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ef222-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ef222-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="ef222-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef222-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ef222-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef222-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef222-139">**Itparticipantsubstreamcontrol**</span><span class="sxs-lookup"><span data-stu-id="ef222-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="ef222-140">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="ef222-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="ef222-141">**Itsubstream**</span><span class="sxs-lookup"><span data-stu-id="ef222-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

