---
description: Die isautoshowenabled-Methode ruft Informationen darüber ab, ob das Videofenster automatisch angezeigt wird, wenn der renderingfilter anhält oder ausgeführt wird.
ms.assetid: 769e3023-a515-4b80-a979-2e4fa9612e65
title: Cbasecontrolwindow. isautoshowenabled-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsAutoShowEnabled
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c4b4a894593cb3be26a1034098cd2a0cdacf926
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368581"
---
# <a name="cbasecontrolwindowisautoshowenabled-method"></a><span data-ttu-id="46dae-103">Cbasecontrolwindow. isautoshowenabled-Methode</span><span class="sxs-lookup"><span data-stu-id="46dae-103">CBaseControlWindow.IsAutoShowEnabled method</span></span>

<span data-ttu-id="46dae-104">Die- `IsAutoShowEnabled` Methode ruft Informationen darüber ab, ob das Videofenster automatisch angezeigt wird, wenn der renderingfilter anhält oder ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46dae-104">The `IsAutoShowEnabled` method retrieves information about whether the video window automatically appears when the rendering filter pauses or runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="46dae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46dae-105">Syntax</span></span>


```C++
BOOL IsAutoShowEnabled();
```



## <a name="parameters"></a><span data-ttu-id="46dae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="46dae-106">Parameters</span></span>

<span data-ttu-id="46dae-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="46dae-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46dae-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46dae-108">Return value</span></span>

<span data-ttu-id="46dae-109">Gibt **true** zurück, wenn das **m \_ bauchanshow** -Element auf 1 oder **false** festgelegt ist, wenn es auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="46dae-109">Returns **TRUE** if the **m\_bAutoShow** member is set to  1 or **FALSE** if it is set to 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="46dae-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46dae-110">Remarks</span></span>

<span data-ttu-id="46dae-111">Wenn das **m \_ baudeshow** -Element in einem ausgeblendeten Videofenster auf 1 festgelegt ist, wird das Fenster sichtbar, wenn der Filter anhält oder ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46dae-111">If the **m\_bAutoShow** member is set to  1 on a video window that is hidden, the window becomes visible when the filter pauses or runs.</span></span> <span data-ttu-id="46dae-112">Wenn dieser Member auf 0 festgelegt ist, wird das Fenster nur angezeigt, wenn Sie die Member-Funktion [**cbasecontrolwindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) oder [**cbasecontrolwindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) mit den entsprechenden Parametern verwenden.</span><span class="sxs-lookup"><span data-stu-id="46dae-112">If this member is set to 0, the window will appear only if you use the [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) member function with the appropriate parameters.</span></span>

<span data-ttu-id="46dae-113">Diese Member-Funktion Ruft die **m \_ baudeshow** -Element Einstellung ab und hat dasselbe Ergebnis wie die Verwendung der [**IVideoWindow:: get \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) -Methode.</span><span class="sxs-lookup"><span data-stu-id="46dae-113">This member function retrieves the **m\_bAutoShow** member setting and has the same result as using the [**IVideoWindow::get\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="46dae-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46dae-114">Requirements</span></span>



| <span data-ttu-id="46dae-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46dae-115">Requirement</span></span> | <span data-ttu-id="46dae-116">Wert</span><span class="sxs-lookup"><span data-stu-id="46dae-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46dae-117">Header</span><span class="sxs-lookup"><span data-stu-id="46dae-117">Header</span></span><br/>  | <dl> <span data-ttu-id="46dae-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46dae-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="46dae-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="46dae-119">Library</span></span><br/> | <dl> <span data-ttu-id="46dae-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="46dae-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46dae-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46dae-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46dae-122">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="46dae-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




