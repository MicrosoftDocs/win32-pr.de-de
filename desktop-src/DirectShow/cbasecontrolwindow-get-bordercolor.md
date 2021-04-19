---
description: Die get \_ BorderColor-Methode ruft die aktuelle Rahmenfarbe ab.
ms.assetid: 4b4cae1d-bef7-4f8d-8011-c220fcfb73eb
title: CBaseControlWindow.get_BorderColor-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d889f211b204c2c0180ae757a0240c8588552e83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359254"
---
# <a name="cbasecontrolwindowget_bordercolor-method"></a><span data-ttu-id="a77f3-103">Cbasecontrolwindow. get \_ BorderColor-Methode</span><span class="sxs-lookup"><span data-stu-id="a77f3-103">CBaseControlWindow.get\_BorderColor method</span></span>

<span data-ttu-id="a77f3-104">Die- `get_BorderColor` Methode ruft die aktuelle Rahmenfarbe ab.</span><span class="sxs-lookup"><span data-stu-id="a77f3-104">The `get_BorderColor` method retrieves the current border color.</span></span>

## <a name="syntax"></a><span data-ttu-id="a77f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a77f3-105">Syntax</span></span>


```C++
HRESULT get_BorderColor(
   long *Color
);
```



## <a name="parameters"></a><span data-ttu-id="a77f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a77f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a77f3-107">*Farbe*</span><span class="sxs-lookup"><span data-stu-id="a77f3-107">*Color*</span></span> 
</dt> <dd>

<span data-ttu-id="a77f3-108">Zeiger auf die aktuelle Rahmenfarbe.</span><span class="sxs-lookup"><span data-stu-id="a77f3-108">Pointer to the current border color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a77f3-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a77f3-109">Return value</span></span>

<span data-ttu-id="a77f3-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a77f3-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a77f3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a77f3-111">Remarks</span></span>

<span data-ttu-id="a77f3-112">Eine Anwendung kann ein Ziel Rechteck festlegen, in dem das Video angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a77f3-112">An application can set a destination rectangle in which the video should be displayed.</span></span> <span data-ttu-id="a77f3-113">Dieses Rechteck ist relativ zum Client Bereich des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a77f3-113">This rectangle is relative to the client area for the window.</span></span> <span data-ttu-id="a77f3-114">Wenn dies geschieht (Standardmäßig wird das gesamte Fenster gezeichnet), gibt es einen Rahmen, der das Video umgibt.</span><span class="sxs-lookup"><span data-stu-id="a77f3-114">If this is done (the default is to always paint the entire window), there is a border surrounding the video.</span></span> <span data-ttu-id="a77f3-115">Diese Eigenschaft wirkt sich auf die vom Rahmen verwendete Farbe aus.</span><span class="sxs-lookup"><span data-stu-id="a77f3-115">This property affects the color used by the border.</span></span> <span data-ttu-id="a77f3-116">Obwohl der-Parameter als **Long** -Typ angegeben ist, handelt es sich tatsächlich um einen **COLORREF** -Wert.</span><span class="sxs-lookup"><span data-stu-id="a77f3-116">Although the parameter is specified as a **LONG** type, it is actually a **COLORREF** value.</span></span>

<span data-ttu-id="a77f3-117">Diese Member-Funktion soll von externen Objekten über die [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle aufgerufen werden und sperrt daher den kritischen Abschnitt, um mit dem zugeordneten Filter synchronisiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="a77f3-117">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="a77f3-118">Rufen Sie die Member-Funktion [**cbasecontrolwindow:: getBorderColor**](cbasecontrolwindow-getbordercolour.md) auf, um diese Eigenschaft abzurufen, wenn Sie nicht von einem externen Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a77f3-118">Call the [**CBaseControlWindow::GetBorderColour**](cbasecontrolwindow-getbordercolour.md) member function to retrieve this property if not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="a77f3-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a77f3-119">Requirements</span></span>



| <span data-ttu-id="a77f3-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a77f3-120">Requirement</span></span> | <span data-ttu-id="a77f3-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a77f3-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a77f3-122">Header</span><span class="sxs-lookup"><span data-stu-id="a77f3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a77f3-123"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a77f3-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a77f3-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a77f3-124">Library</span></span><br/> | <dl> <span data-ttu-id="a77f3-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a77f3-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a77f3-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a77f3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a77f3-127">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a77f3-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




