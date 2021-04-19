---
description: Die OnSize-Methode verarbeitet \_ Nachrichten der WM-Größe.
ms.assetid: 21d867a4-4321-478a-9beb-5d3053569369
title: Cbasewindow. OnSize-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9020510030d3b3d4b30e066adfe67367618fb3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365969"
---
# <a name="cbasewindowonsize-method"></a><span data-ttu-id="00f61-103">Cbasewindow. OnSize-Methode</span><span class="sxs-lookup"><span data-stu-id="00f61-103">CBaseWindow.OnSize method</span></span>

<span data-ttu-id="00f61-104">Die- `OnSize` Methode verarbeitet \_ Nachrichten der WM-Größe.</span><span class="sxs-lookup"><span data-stu-id="00f61-104">The `OnSize` method handles WM\_SIZE messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="00f61-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="00f61-105">Syntax</span></span>


```C++
virtual BOOL OnSize(
   LONG Width,
   LONG Height
);
```



## <a name="parameters"></a><span data-ttu-id="00f61-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="00f61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00f61-107">*Width*</span><span class="sxs-lookup"><span data-stu-id="00f61-107">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="00f61-108">Breite des Client Bereichs in Pixel.</span><span class="sxs-lookup"><span data-stu-id="00f61-108">Width of the client area, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="00f61-109">*Height*</span><span class="sxs-lookup"><span data-stu-id="00f61-109">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="00f61-110">Die Höhe des Client Bereichs in Pixel.</span><span class="sxs-lookup"><span data-stu-id="00f61-110">Height of the client area, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00f61-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00f61-111">Return value</span></span>

<span data-ttu-id="00f61-112">Gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="00f61-112">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="00f61-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00f61-113">Remarks</span></span>

<span data-ttu-id="00f61-114">Diese Methode speichert die neue Breite und Höhe.</span><span class="sxs-lookup"><span data-stu-id="00f61-114">This method stores the new width and height.</span></span> <span data-ttu-id="00f61-115">Um diese Werte abzurufen, rufen Sie die [**cbasewindow:: getwindowheight**](cbasewindow-getwindowheight.md) -Methode und die [**cbasewindow:: getwindowwidth**](cbasewindow-getwindowwidth.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="00f61-115">To retrieve these values, call the [**CBaseWindow::GetWindowHeight**](cbasewindow-getwindowheight.md) and [**CBaseWindow::GetWindowWidth**](cbasewindow-getwindowwidth.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="00f61-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00f61-116">Requirements</span></span>



| <span data-ttu-id="00f61-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00f61-117">Requirement</span></span> | <span data-ttu-id="00f61-118">Wert</span><span class="sxs-lookup"><span data-stu-id="00f61-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00f61-119">Header</span><span class="sxs-lookup"><span data-stu-id="00f61-119">Header</span></span><br/>  | <dl> <span data-ttu-id="00f61-120"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00f61-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="00f61-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="00f61-121">Library</span></span><br/> | <dl> <span data-ttu-id="00f61-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="00f61-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00f61-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00f61-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00f61-124">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="00f61-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




