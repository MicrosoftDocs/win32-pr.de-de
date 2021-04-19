---
description: Die onpalettechange-Methode verarbeitet palettenänderungs Meldungen.
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: Cbasewindow. onpalettechange-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnPaletteChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9abcb2d9f5cdc875f70f5c1db1fd2f625ce911f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369441"
---
# <a name="cbasewindowonpalettechange-method"></a><span data-ttu-id="d9bef-103">Cbasewindow. onpalettechange-Methode</span><span class="sxs-lookup"><span data-stu-id="d9bef-103">CBaseWindow.OnPaletteChange method</span></span>

<span data-ttu-id="d9bef-104">Die `OnPaletteChange` -Methode verarbeitet palettenänderungs Meldungen.</span><span class="sxs-lookup"><span data-stu-id="d9bef-104">The `OnPaletteChange` method handles palette-change messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9bef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9bef-105">Syntax</span></span>


```C++
virtual LRESULT OnPaletteChange(
   HWND hwnd,
   UINT Message
);
```



## <a name="parameters"></a><span data-ttu-id="d9bef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9bef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9bef-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="d9bef-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d9bef-108">Handle für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="d9bef-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="d9bef-109">*Meldung*</span><span class="sxs-lookup"><span data-stu-id="d9bef-109">*Message*</span></span> 
</dt> <dd>

<span data-ttu-id="d9bef-110">Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="d9bef-110">Message identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9bef-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9bef-111">Return value</span></span>

<span data-ttu-id="d9bef-112">Gibt 0 zurück, wenn die Meldung verarbeitet wurde, oder 1, wenn die Meldung nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="d9bef-112">Returns 0 if the message was processed, or 1 if the message was not processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9bef-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9bef-113">Remarks</span></span>

<span data-ttu-id="d9bef-114">Diese Methode verarbeitet die \_ Nachrichten "WM palettechanged" und "WM \_ querynewpalette".</span><span class="sxs-lookup"><span data-stu-id="d9bef-114">This method handles WM\_PALETTECHANGED and WM\_QUERYNEWPALETTE messages.</span></span> <span data-ttu-id="d9bef-115">Die [**cbasewindow::D orealisetpalette**](cbasewindow-dorealisepalette.md) -Methode wird aufgerufen, um die neue Palette zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="d9bef-115">It calls the [**CBaseWindow::DoRealisePalette**](cbasewindow-dorealisepalette.md) method to realize the new palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9bef-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9bef-116">Requirements</span></span>



| <span data-ttu-id="d9bef-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9bef-117">Requirement</span></span> | <span data-ttu-id="d9bef-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d9bef-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9bef-119">Header</span><span class="sxs-lookup"><span data-stu-id="d9bef-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d9bef-120"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9bef-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d9bef-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d9bef-121">Library</span></span><br/> | <dl> <span data-ttu-id="d9bef-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d9bef-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9bef-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9bef-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9bef-124">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d9bef-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




