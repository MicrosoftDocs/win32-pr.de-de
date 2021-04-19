---
description: Die get \_ Streams-Methode erstellt eine Auflistung von Streams, die dem aktuellen Teilnehmer zugeordnet sind.
ms.assetid: 9ab05b14-8ef8-4e7f-b598-05795011e35d
title: 'Itteilnehmer:: get_Streams-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a920929c71e01632edcd8c4c78029b479d8b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368527"
---
# <a name="itparticipantget_streams-method"></a><span data-ttu-id="e0486-103">Itteilnehmer:: get \_ Streams-Methode</span><span class="sxs-lookup"><span data-stu-id="e0486-103">ITParticipant::get\_Streams method</span></span>

<span data-ttu-id="e0486-104">\[**get \_ Streams** sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e0486-104">\[**get\_Streams** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e0486-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="e0486-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e0486-106">Die **get \_ Streams** -Methode erstellt eine Auflistung von Streams, die dem aktuellen Teilnehmer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e0486-106">The **get\_Streams** method creates a collection of streams associated with the current participant.</span></span> <span data-ttu-id="e0486-107">Diese Methode wird für Automatisierungs Client Anwendungen bereitgestellt, wie z. b. in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e0486-107">This method is provided for Automation client applications, such as those written in Visual Basic.</span></span> <span data-ttu-id="e0486-108">C-und C++-Anwendungen müssen die [**enumeratestreams**](itparticipant-enumeratestreams.md) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0486-108">C and C++ applications must use the [**EnumerateStreams**](itparticipant-enumeratestreams.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0486-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0486-109">Syntax</span></span>


```C++
HRESULT get_Streams(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a><span data-ttu-id="e0486-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0486-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0486-111">*pvariant* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e0486-111">*pVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0486-112">Ein Zeiger auf eine **Variante** , die eine [**itcollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) von [**itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) -Schnittstellen Zeigern enthält.</span><span class="sxs-lookup"><span data-stu-id="e0486-112">Pointer to **VARIANT** containing an [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) of [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0486-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0486-113">Return value</span></span>

<span data-ttu-id="e0486-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e0486-114">This method can return one of these values.</span></span>



| <span data-ttu-id="e0486-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e0486-115">Value</span></span>                                                                                         | <span data-ttu-id="e0486-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e0486-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e0486-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e0486-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e0486-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e0486-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e0486-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="e0486-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e0486-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e0486-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e0486-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="e0486-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e0486-122">Der *pvariant* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="e0486-122">The *pVariant* parameter is not a valid pointer.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="e0486-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0486-123">Remarks</span></span>

<span data-ttu-id="e0486-124">TAPI Ruft die **adressf** -Methode für die [**itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) -Schnittstelle auf, die von **itparticipants:: get \_ Streams** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e0486-124">TAPI calls the **AddRef** method on the [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface returned by **ITParticipant::get\_Streams**.</span></span> <span data-ttu-id="e0486-125">Die Anwendung muss Release auf der **itstream** -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e0486-125">The application must call **Release** on the **ITStream** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0486-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0486-126">Requirements</span></span>



| <span data-ttu-id="e0486-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0486-127">Requirement</span></span> | <span data-ttu-id="e0486-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e0486-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0486-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="e0486-129">TAPI version</span></span><br/> | <span data-ttu-id="e0486-130">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e0486-130">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="e0486-131">Header</span><span class="sxs-lookup"><span data-stu-id="e0486-131">Header</span></span><br/>       | <dl> <span data-ttu-id="e0486-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0486-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0486-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e0486-133">Library</span></span><br/>      | <dl> <span data-ttu-id="e0486-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0486-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="e0486-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e0486-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="e0486-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0486-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0486-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0486-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0486-138">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="e0486-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="e0486-139">**Enumeratestreams**</span><span class="sxs-lookup"><span data-stu-id="e0486-139">**EnumerateStreams**</span></span>](itparticipant-enumeratestreams.md)
</dt> <dt>

[<span data-ttu-id="e0486-140">**Ienumstream**</span><span class="sxs-lookup"><span data-stu-id="e0486-140">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[<span data-ttu-id="e0486-141">**Itcollection**</span><span class="sxs-lookup"><span data-stu-id="e0486-141">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[<span data-ttu-id="e0486-142">**Itstream**</span><span class="sxs-lookup"><span data-stu-id="e0486-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

