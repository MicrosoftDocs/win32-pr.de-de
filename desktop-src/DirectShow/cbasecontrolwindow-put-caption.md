---
description: Die Put \_ Caption-Methode legt den Titel oder die Beschriftung des Fensters fest.
ms.assetid: 6671805a-e1ef-40f1-bc3f-bf7954ff9851
title: CBaseControlWindow.put_Caption-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aca8e5e7ad04acae9fab1cfe2d44f982266805e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368435"
---
# <a name="cbasecontrolwindowput_caption-method"></a><span data-ttu-id="94849-103">Cbasecontrolwindow. Put- \_ Beschriftungs Methode</span><span class="sxs-lookup"><span data-stu-id="94849-103">CBaseControlWindow.put\_Caption method</span></span>

<span data-ttu-id="94849-104">Die- `put_Caption` Methode legt den Titel oder die Beschriftung des Fensters fest.</span><span class="sxs-lookup"><span data-stu-id="94849-104">The `put_Caption` method sets the window title or caption.</span></span>

## <a name="syntax"></a><span data-ttu-id="94849-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="94849-105">Syntax</span></span>


```C++
HRESULT put_Caption(
   BSTR strCaption
);
```



## <a name="parameters"></a><span data-ttu-id="94849-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="94849-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94849-107">*Überschrift*</span><span class="sxs-lookup"><span data-stu-id="94849-107">*strCaption*</span></span> 
</dt> <dd>

<span data-ttu-id="94849-108">Neue Fenster Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="94849-108">New window caption.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94849-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94849-109">Return value</span></span>

<span data-ttu-id="94849-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="94849-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94849-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94849-111">Remarks</span></span>

<span data-ttu-id="94849-112">Den meisten Fenstern der obersten Ebene auf einem Windows-basierten Desktop ist ein Titel (Beschriftung) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="94849-112">Most top-level windows on a Windows-based desktop have a title (caption) associated with them.</span></span> <span data-ttu-id="94849-113">Diese Eigenschaft kann durch die [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle abgefragt und festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="94849-113">This property can be queried and set through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="94849-114">Jeder Beschriftungs Satz ist nur sichtbar, wenn für das Fenster der WS- \_ Beschriftungs Stil angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="94849-114">Any caption set will be visible only if the window has the WS\_CAPTION style applied.</span></span> <span data-ttu-id="94849-115">Wenn dies nicht der Fall ist, kann die Beschriftung weiterhin festgelegt (und abgerufen) werden, auch wenn Sie für den Benutzer nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="94849-115">If it does not, the caption can still be set (and retrieved), although it will not be visible to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="94849-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94849-116">Requirements</span></span>



| <span data-ttu-id="94849-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94849-117">Requirement</span></span> | <span data-ttu-id="94849-118">Wert</span><span class="sxs-lookup"><span data-stu-id="94849-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94849-119">Header</span><span class="sxs-lookup"><span data-stu-id="94849-119">Header</span></span><br/>  | <dl> <span data-ttu-id="94849-120"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94849-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="94849-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="94849-121">Library</span></span><br/> | <dl> <span data-ttu-id="94849-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="94849-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94849-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94849-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94849-124">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="94849-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




