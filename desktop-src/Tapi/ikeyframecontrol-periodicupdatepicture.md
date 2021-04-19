---
description: Die periodicupdatepicture-Methode wird von einer Anwendung aufgerufen, um einen Timer im Stream zu konfigurieren, der regelmäßig Bildaktualisierungen anfordert. Bildaktualisierungen führen zu einer hohen Bandbreitenauslastung, sodass diese Methode normalerweise anstelle von Update Picture verwendet wird.
ms.assetid: 6ae3b5e9-bc11-4f3f-972b-21c9ac299987
title: Ikeyframecontrol::P eriodicupdatepicture-Methode (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bbfb18b0be96d611f0fe385cc825602dc316ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352840"
---
# <a name="ikeyframecontrolperiodicupdatepicture-method"></a><span data-ttu-id="3f285-104">Ikeyframecontrol::P eriodicupdatepicture-Methode</span><span class="sxs-lookup"><span data-stu-id="3f285-104">IKeyFrameControl::PeriodicUpdatePicture method</span></span>

<span data-ttu-id="3f285-105">\[**Periodicupdatepicture** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3f285-105">\[**PeriodicUpdatePicture** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3f285-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="3f285-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3f285-107">Die **periodicupdatepicture** -Methode wird von einer Anwendung aufgerufen, um einen Timer im Stream zu konfigurieren, der regelmäßig Bildaktualisierungen anfordert.</span><span class="sxs-lookup"><span data-stu-id="3f285-107">The **PeriodicUpdatePicture** method is called by an application to configure a timer in the stream that will ask for picture updates periodically.</span></span> <span data-ttu-id="3f285-108">Bildaktualisierungen führen zu einer hohen Bandbreitenauslastung, sodass diese Methode normalerweise anstelle von [**Update Picture**](ikeyframecontrol-updatepicture.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3f285-108">Picture updates cause high bandwidth usage, so this method will normally be used instead of [**UpdatePicture**](ikeyframecontrol-updatepicture.md).</span></span>

<span data-ttu-id="3f285-109">Wenn die-Methode aufgerufen wird, wenn der Stream aktiv ist, wird der Timer sofort gestartet.</span><span class="sxs-lookup"><span data-stu-id="3f285-109">If the method is called when the stream is active, the timer will start immediately.</span></span> <span data-ttu-id="3f285-110">Wenn der Stream nicht aktiv ist, wird der Timer gestartet, wenn der Stream in den aktiven Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="3f285-110">If the stream is not active, the timer will be started when the stream enters the active state.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f285-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f285-111">Syntax</span></span>


```C++
HRESULT PeriodicUpdatePicture(
  [in] BOOL  fEnable,
  [in] DWORD dwInterval
);
```



## <a name="parameters"></a><span data-ttu-id="3f285-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f285-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f285-113">*fenckbar* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f285-113">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f285-114">**True** aktiviert den Timer.</span><span class="sxs-lookup"><span data-stu-id="3f285-114">**TRUE** enables the timer.</span></span> <span data-ttu-id="3f285-115">**False** deaktiviert es.</span><span class="sxs-lookup"><span data-stu-id="3f285-115">**FALSE** disables it.</span></span>

</dd> <dt>

<span data-ttu-id="3f285-116">*dwinterval* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f285-116">*dwInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f285-117">Das Intervall für den Timer in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="3f285-117">The interval for the timer, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f285-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f285-118">Return value</span></span>

<span data-ttu-id="3f285-119">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3f285-119">This method can return one of these values.</span></span>



| <span data-ttu-id="3f285-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3f285-120">Return code</span></span>                                                                            | <span data-ttu-id="3f285-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f285-121">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="3f285-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3f285-122"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="3f285-123">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3f285-123">Method succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="3f285-124"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="3f285-124"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="3f285-125">Unerwartete Gründe sind aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="3f285-125">Failed for unexpected reasons.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3f285-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f285-126">Requirements</span></span>



| <span data-ttu-id="3f285-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f285-127">Requirement</span></span> | <span data-ttu-id="3f285-128">Wert</span><span class="sxs-lookup"><span data-stu-id="3f285-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f285-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="3f285-129">TAPI version</span></span><br/> | <span data-ttu-id="3f285-130">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="3f285-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3f285-131">Header</span><span class="sxs-lookup"><span data-stu-id="3f285-131">Header</span></span><br/>       | <dl> <span data-ttu-id="3f285-132"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f285-132"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="3f285-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3f285-133">Library</span></span><br/>      | <dl> <span data-ttu-id="3f285-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f285-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3f285-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3f285-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="3f285-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f285-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3f285-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f285-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f285-138">H323-msp</span><span class="sxs-lookup"><span data-stu-id="3f285-138">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

 




