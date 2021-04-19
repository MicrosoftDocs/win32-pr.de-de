---
description: Der Anzeigemodus wurde geändert.
ms.assetid: 1f5b066b-6d5d-44bb-851a-424b2bd389c0
title: EC_DISPLAY_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549a4c5201906b692a1bd726e65269679705e9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356016"
---
# <a name="ec_display_changed"></a><span data-ttu-id="82c9b-103">EC- \_ Anzeige \_ geändert</span><span class="sxs-lookup"><span data-stu-id="82c9b-103">EC\_DISPLAY\_CHANGED</span></span>

<span data-ttu-id="82c9b-104">Der Anzeigemodus wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="82c9b-104">The display mode has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="82c9b-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="82c9b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82c9b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="82c9b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="82c9b-107">(**IUnknown** \* ) Zeiger auf ein Array von [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstellen für die Eingabe Pins des Video-Renderers.</span><span class="sxs-lookup"><span data-stu-id="82c9b-107">(**IUnknown**\*) Pointer to an array of [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interfaces for the video renderer's input pins.</span></span> <span data-ttu-id="82c9b-108">Wenn *lParam2* NULL ist, kann dieser Parameter **null** sein.</span><span class="sxs-lookup"><span data-stu-id="82c9b-108">If *lParam2* is zero, this parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="82c9b-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="82c9b-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="82c9b-110">Wenn *lParam2* NULL ist, enthält *lParam1* einen einzelnen **IPin** -Zeiger oder ist gleich **null**.</span><span class="sxs-lookup"><span data-stu-id="82c9b-110">If *lParam2* is zero, *lParam1* contains a single **IPin** pointer or equals **NULL**.</span></span> <span data-ttu-id="82c9b-111">Wenn *lParam2* größer als 0 (null) ist, enthält *lParam1* ein Array von **IPin** -Zeigern, und die Anzahl der Elemente im Array wird von *lParam2* angegeben.</span><span class="sxs-lookup"><span data-stu-id="82c9b-111">If *lParam2* is greater than zero, *lParam1* contains an array of **IPin** pointers, and the number of elements in the array is given by *lParam2*.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="82c9b-112">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="82c9b-112">Default Action</span></span>

<span data-ttu-id="82c9b-113">Der Filter Graph-Manager stoppt das Diagramm temporär und trennt dann die Verbindung mit dem Videorenderer und stellt die Verbindung wieder her.</span><span class="sxs-lookup"><span data-stu-id="82c9b-113">The filter graph manager temporarily stops the graph, and then disconnects and reconnects the video renderer.</span></span> <span data-ttu-id="82c9b-114">Das Ereignis wird nicht an die Anwendung übergeben.</span><span class="sxs-lookup"><span data-stu-id="82c9b-114">It does not pass the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="82c9b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82c9b-115">Remarks</span></span>

<span data-ttu-id="82c9b-116">Videorenderer können dieses Ereignis als Antwort auf eine WM- [**\_ displaychange**](/windows/desktop/gdi/wm-displaychange) -Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="82c9b-116">Video renderers can send this event in response to a [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) message.</span></span> <span data-ttu-id="82c9b-117">Die Meldung " **WM \_ displaychange** " gibt an, dass der Benutzer die Bildschirmauflösung geändert hat.</span><span class="sxs-lookup"><span data-stu-id="82c9b-117">The **WM\_DISPLAYCHANGE** message indicates that the user has changed the display resolution.</span></span>

<span data-ttu-id="82c9b-118">Während der Pin-Verbindung wählen die meisten Videorenderer ein Format aus, das auf dem aktuellen Anzeigemodus basiert.</span><span class="sxs-lookup"><span data-stu-id="82c9b-118">During pin connection, most video renderers pick a format based on the current display mode.</span></span> <span data-ttu-id="82c9b-119">Wenn sich der Anzeigemodus ändert, muss der Videorenderer möglicherweise ein anderes Format auswählen.</span><span class="sxs-lookup"><span data-stu-id="82c9b-119">If the display mode changes, the video renderer might need to choose another format.</span></span> <span data-ttu-id="82c9b-120">Durch Senden dieser Nachricht signalisiert der Renderer dem Filter Graph-Manager, dass er erneut verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="82c9b-120">By sending this message, the renderer signals to the filter graph manager that it needs to be reconnected.</span></span> <span data-ttu-id="82c9b-121">Während der erneuten Verbindung kann der Renderer ein neues Format auswählen.</span><span class="sxs-lookup"><span data-stu-id="82c9b-121">During the reconnection, the renderer can select a new format.</span></span> <span data-ttu-id="82c9b-122">Wenn die erneute Verbindungs Herstellung fehlschlägt, sendet der Filter Graph-Manager ein [**EC \_ errorabort**](ec-errorabort.md) -Ereignis an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="82c9b-122">If the reconnection fails, the filter graph manager sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the application.</span></span>

### <a name="enhanced-video-renderer"></a><span data-ttu-id="82c9b-123">Erweiterter Videorenderer</span><span class="sxs-lookup"><span data-stu-id="82c9b-123">Enhanced Video Renderer</span></span>

<span data-ttu-id="82c9b-124">Ein benutzerdefinierter Presenter für den [**erweiterten Videorenderer**](enhanced-video-renderer-filter.md) (EVR) sollte dieses Ereignis an den EVR senden, wenn sich das Direct3D-Gerät des Presenter ändert.</span><span class="sxs-lookup"><span data-stu-id="82c9b-124">A custom presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) should send this event to the EVR if the presenter's Direct3D device changes.</span></span> <span data-ttu-id="82c9b-125">Legen Sie *lParam1* und *lParam2* auf 0 (null) fest. der EVR ignoriert die Ereignis Parameter.</span><span class="sxs-lookup"><span data-stu-id="82c9b-125">Set *lParam1* and *lParam2* to zero; the EVR ignores the event parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="82c9b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82c9b-126">Requirements</span></span>



| <span data-ttu-id="82c9b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82c9b-127">Requirement</span></span> | <span data-ttu-id="82c9b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="82c9b-128">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="82c9b-129">Header</span><span class="sxs-lookup"><span data-stu-id="82c9b-129">Header</span></span><br/> | <dl> <span data-ttu-id="82c9b-130"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="82c9b-130"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82c9b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82c9b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82c9b-132">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="82c9b-132">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="82c9b-133">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="82c9b-133">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

