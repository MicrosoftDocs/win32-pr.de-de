---
description: Mit der enumeratestreams-Methode werden Datenströme aufgelistet, die derzeit mit den Teilnehmern erstellt werden. Diese Methode wird für C-und C++-Anwendungen bereitgestellt. Automatisierungs Client Anwendungen, wie z. b. die in Visual Basic geschriebenen, müssen die get \_ Streams-Methode verwenden.
ms.assetid: 69db198d-fb4c-482b-bf49-5c636ac2f86b
title: 'Itparticipants:: enumeratestreams-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbc92c617ed4baee3ecc33aec65cbdcf50986a27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358646"
---
# <a name="itparticipantenumeratestreams-method"></a><span data-ttu-id="678a0-105">Itparticipants:: enumeratestreams-Methode</span><span class="sxs-lookup"><span data-stu-id="678a0-105">ITParticipant::EnumerateStreams method</span></span>

<span data-ttu-id="678a0-106">\[**Enumeratestreams** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="678a0-106">\[**EnumerateStreams** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="678a0-107">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="678a0-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="678a0-108">Mit der **enumeratestreams** -Methode werden Datenströme aufgelistet, die derzeit mit den Teilnehmern erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="678a0-108">The **EnumerateStreams** method enumerates streams currently with the participants.</span></span> <span data-ttu-id="678a0-109">Diese Methode wird für C-und C++-Anwendungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="678a0-109">This method is provided for C and C++ applications.</span></span> <span data-ttu-id="678a0-110">Automatisierungs Client Anwendungen, wie z. b. die in Visual Basic geschriebenen, müssen die [**get \_ Streams**](itparticipant-get-streams.md) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="678a0-110">Automation client applications, such as those written in Visual Basic, must use the [**get\_Streams**](itparticipant-get-streams.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="678a0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="678a0-111">Syntax</span></span>


```C++
HRESULT EnumerateStreams(
  [out] IEnumStream **ppEnumStream
);
```



## <a name="parameters"></a><span data-ttu-id="678a0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="678a0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="678a0-113">" *pprestream* \[ " vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="678a0-113">*ppEnumStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="678a0-114">Zeiger auf den [**ienumstream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="678a0-114">Pointer to [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="678a0-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="678a0-115">Return value</span></span>

<span data-ttu-id="678a0-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="678a0-116">This method can return one of these values.</span></span>



| <span data-ttu-id="678a0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="678a0-117">Value</span></span>                                                                                     | <span data-ttu-id="678a0-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="678a0-118">Meaning</span></span>                                                         |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="678a0-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="678a0-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="678a0-120">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="678a0-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="678a0-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="678a0-121"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="678a0-122">Der Parameter " *dereumstream* " ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="678a0-122">The *ppEnumStream* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="678a0-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="678a0-123">Remarks</span></span>

<span data-ttu-id="678a0-124">TAPI Ruft die **adressf** -Methode für die [**ienumstream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) -Schnittstelle auf, die von **itparticipants:: enumeratestreams** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="678a0-124">TAPI calls the **AddRef** method on the [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) interface returned by **ITParticipant::EnumerateStreams**.</span></span> <span data-ttu-id="678a0-125">Die Anwendung muss Release auf der **ienumstream** -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="678a0-125">The application must call **Release** on the **IEnumStream** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="678a0-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="678a0-126">Requirements</span></span>



| <span data-ttu-id="678a0-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="678a0-127">Requirement</span></span> | <span data-ttu-id="678a0-128">Wert</span><span class="sxs-lookup"><span data-stu-id="678a0-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="678a0-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="678a0-129">TAPI version</span></span><br/> | <span data-ttu-id="678a0-130">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="678a0-130">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="678a0-131">Header</span><span class="sxs-lookup"><span data-stu-id="678a0-131">Header</span></span><br/>       | <dl> <span data-ttu-id="678a0-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="678a0-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="678a0-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="678a0-133">Library</span></span><br/>      | <dl> <span data-ttu-id="678a0-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="678a0-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="678a0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="678a0-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="678a0-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="678a0-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="678a0-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="678a0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="678a0-138">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="678a0-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="678a0-139">**Daten \_ Ströme erhalten**</span><span class="sxs-lookup"><span data-stu-id="678a0-139">**get\_Streams**</span></span>](itparticipant-get-streams.md)
</dt> <dt>

[<span data-ttu-id="678a0-140">**Ienumstream**</span><span class="sxs-lookup"><span data-stu-id="678a0-140">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> </dl>

 

 




