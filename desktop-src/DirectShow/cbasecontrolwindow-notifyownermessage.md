---
description: Die notifyownermessage-Methode übergibt bestimmte Nachrichten an das Videofenster.
ms.assetid: 8b27281a-5b8a-46c3-aa66-390d4496f30e
title: Cbasecontrolwindow. notilyownermessage-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.NotifyOwnerMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9073d37987404849ba8aa3acbda9919df840b410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361066"
---
# <a name="cbasecontrolwindownotifyownermessage-method"></a><span data-ttu-id="c9d68-103">Cbasecontrolwindow. notif yownermessage-Methode</span><span class="sxs-lookup"><span data-stu-id="c9d68-103">CBaseControlWindow.NotifyOwnerMessage method</span></span>

<span data-ttu-id="c9d68-104">Die- `NotifyOwnerMessage` Methode übergibt bestimmte Meldungen an das Videofenster.</span><span class="sxs-lookup"><span data-stu-id="c9d68-104">The `NotifyOwnerMessage` method passes along specific messages to the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9d68-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9d68-105">Syntax</span></span>


```C++
HRESULT NotifyOwnerMessage(
   long     hwnd,
   long     uMsg,
   LONG_PTR wParam,
   LONG_PTR lParam
);
```



## <a name="parameters"></a><span data-ttu-id="c9d68-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9d68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9d68-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="c9d68-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="c9d68-108">Handle für das Videofenster.</span><span class="sxs-lookup"><span data-stu-id="c9d68-108">Handle to the video window.</span></span>

</dd> <dt>

<span data-ttu-id="c9d68-109">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="c9d68-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="c9d68-110">Nachrichten Details.</span><span class="sxs-lookup"><span data-stu-id="c9d68-110">Message details.</span></span>

</dd> <dt>

<span data-ttu-id="c9d68-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9d68-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9d68-112">Der erste Message-Parameter.</span><span class="sxs-lookup"><span data-stu-id="c9d68-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c9d68-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9d68-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9d68-114">Der zweite Meldungs Parameter.</span><span class="sxs-lookup"><span data-stu-id="c9d68-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9d68-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9d68-115">Return value</span></span>

<span data-ttu-id="c9d68-116">Gibt keinen \_ Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="c9d68-116">Returns NO\_ERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9d68-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9d68-117">Remarks</span></span>

<span data-ttu-id="c9d68-118">Wenn das Videofenster ein untergeordnetes Element eines anderen Fensters ist, empfängt es bestimmte Fenster Nachrichten der obersten Ebene nicht.</span><span class="sxs-lookup"><span data-stu-id="c9d68-118">When the video window is a child of another window, it does not receive certain top-level window messages.</span></span> <span data-ttu-id="c9d68-119">Diese Nachrichten können für einen Renderer von Bedeutung sein, da Sie sich auf das Verhalten auswirken könnten.</span><span class="sxs-lookup"><span data-stu-id="c9d68-119">These messages can be valuable to a renderer, because they could affect its behavior.</span></span> <span data-ttu-id="c9d68-120">`NotifyOwnerMessage` übergibt eine der folgenden Meldungen an das Videofenster.</span><span class="sxs-lookup"><span data-stu-id="c9d68-120">`NotifyOwnerMessage` passes any of the following messages to the video window.</span></span>

-   <span data-ttu-id="c9d68-121">WM \_ activateapp</span><span class="sxs-lookup"><span data-stu-id="c9d68-121">WM\_ACTIVATEAPP</span></span>
-   <span data-ttu-id="c9d68-122">WM \_ devmodechange</span><span class="sxs-lookup"><span data-stu-id="c9d68-122">WM\_DEVMODECHANGE</span></span>
-   <span data-ttu-id="c9d68-123">WM- \_ Display Change</span><span class="sxs-lookup"><span data-stu-id="c9d68-123">WM\_DISPLAYCHANGE</span></span>
-   <span data-ttu-id="c9d68-124">WM \_ palettechanged</span><span class="sxs-lookup"><span data-stu-id="c9d68-124">WM\_PALETTECHANGED</span></span>
-   <span data-ttu-id="c9d68-125">WM- \_ paletteischanging</span><span class="sxs-lookup"><span data-stu-id="c9d68-125">WM\_PALETTEISCHANGING</span></span>
-   <span data-ttu-id="c9d68-126">WM \_ querynewpalette</span><span class="sxs-lookup"><span data-stu-id="c9d68-126">WM\_QUERYNEWPALETTE</span></span>
-   <span data-ttu-id="c9d68-127">WM- \_ syscolorchange</span><span class="sxs-lookup"><span data-stu-id="c9d68-127">WM\_SYSCOLORCHANGE</span></span>

<span data-ttu-id="c9d68-128">Sie können anfordern, dass der [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Plug-in-Verteiler (PID) ein Fenster einem anderen Fenster untergeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="c9d68-128">You can request that the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) plug-in distributor (PID) make a window become a child of another window.</span></span> <span data-ttu-id="c9d68-129">Wenn dies auftritt, sucht die PID nach bestimmten Nachrichten, die möglicherweise an das besitzende Fenster gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9d68-129">When this occurs, the PID will look for certain messages that might be sent to the owning window.</span></span> <span data-ttu-id="c9d68-130">Die PID führt diese Nachrichten dann an das eigene Fenster weiter.</span><span class="sxs-lookup"><span data-stu-id="c9d68-130">The PID will then forward those messages to the owned window.</span></span> <span data-ttu-id="c9d68-131">Die Standard Verarbeitung für die Nachrichten besteht darin, Sie synchron an die eigene Fenster Prozedur zu senden, indem Sie die Win32 **SendMessage** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c9d68-131">The default processing for the messages is to send them to the owned window procedure synchronously by calling the Win32 **SendMessage** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9d68-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9d68-132">Requirements</span></span>



| <span data-ttu-id="c9d68-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9d68-133">Requirement</span></span> | <span data-ttu-id="c9d68-134">Wert</span><span class="sxs-lookup"><span data-stu-id="c9d68-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d68-135">Header</span><span class="sxs-lookup"><span data-stu-id="c9d68-135">Header</span></span><br/>  | <dl> <span data-ttu-id="c9d68-136"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9d68-136"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c9d68-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c9d68-137">Library</span></span><br/> | <dl> <span data-ttu-id="c9d68-138">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c9d68-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9d68-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9d68-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9d68-140">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c9d68-140">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




