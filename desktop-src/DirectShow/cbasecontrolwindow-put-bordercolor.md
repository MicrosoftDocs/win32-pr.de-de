---
description: Die Put \_ BorderColor-Methode ändert die Rahmenfarbe.
ms.assetid: bb19d338-7fd1-448c-be94-1c71d4a9a330
title: CBaseControlWindow.put_BorderColor-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54db6de704f2ee0fde1a5087e83df4b362a57959
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353004"
---
# <a name="cbasecontrolwindowput_bordercolor-method"></a><span data-ttu-id="13583-103">Cbasecontrolwindow. Put \_ BorderColor-Methode</span><span class="sxs-lookup"><span data-stu-id="13583-103">CBaseControlWindow.put\_BorderColor method</span></span>

<span data-ttu-id="13583-104">Die- `put_BorderColor` Methode ändert die Rahmenfarbe.</span><span class="sxs-lookup"><span data-stu-id="13583-104">The `put_BorderColor` method changes the border color.</span></span>

## <a name="syntax"></a><span data-ttu-id="13583-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="13583-105">Syntax</span></span>


```C++
HRESULT put_BorderColor(
   long Color
);
```



## <a name="parameters"></a><span data-ttu-id="13583-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13583-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13583-107">*Farbe*</span><span class="sxs-lookup"><span data-stu-id="13583-107">*Color*</span></span> 
</dt> <dd>

<span data-ttu-id="13583-108">Neue Rahmenfarbe.</span><span class="sxs-lookup"><span data-stu-id="13583-108">New border color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13583-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13583-109">Return value</span></span>

<span data-ttu-id="13583-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="13583-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13583-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13583-111">Remarks</span></span>

<span data-ttu-id="13583-112">Eine Anwendung kann ein Ziel Rechteck einrichten, in dem das Video angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="13583-112">An application can establish a destination rectangle in which the video should be displayed.</span></span> <span data-ttu-id="13583-113">Dieses Rechteck ist relativ zum Client Bereich des Fensters.</span><span class="sxs-lookup"><span data-stu-id="13583-113">This rectangle is relative to the client area for the window.</span></span> <span data-ttu-id="13583-114">Wenn dies geschieht (Standardmäßig wird das gesamte Fenster gezeichnet), gibt es einen Rahmen, der das Video umgibt.</span><span class="sxs-lookup"><span data-stu-id="13583-114">If this is done (the default is to always paint the entire window), there is a border surrounding the video.</span></span> <span data-ttu-id="13583-115">Diese Eigenschaft wirkt sich auf die vom Rahmen verwendete Farbe aus.</span><span class="sxs-lookup"><span data-stu-id="13583-115">This property affects the color used by the border.</span></span> <span data-ttu-id="13583-116">Obwohl der-Parameter als **Long** -Typ angegeben ist, handelt es sich tatsächlich um einen **COLORREF** -Wert.</span><span class="sxs-lookup"><span data-stu-id="13583-116">Although the parameter is specified as a **LONG** type, it is actually a **COLORREF** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="13583-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13583-117">Requirements</span></span>



| <span data-ttu-id="13583-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13583-118">Requirement</span></span> | <span data-ttu-id="13583-119">Wert</span><span class="sxs-lookup"><span data-stu-id="13583-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13583-120">Header</span><span class="sxs-lookup"><span data-stu-id="13583-120">Header</span></span><br/>  | <dl> <span data-ttu-id="13583-121"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13583-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="13583-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="13583-122">Library</span></span><br/> | <dl> <span data-ttu-id="13583-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="13583-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13583-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13583-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13583-125">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="13583-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




