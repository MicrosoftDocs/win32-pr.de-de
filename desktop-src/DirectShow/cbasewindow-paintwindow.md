---
description: Die paintwindow-Methode bewirkt, dass das Fenster neu gezeichnet wird.
ms.assetid: dce3d782-00e5-4176-9365-378d59d48ebc
title: Cbasewindow. paintwindow-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PaintWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b0932422f85cb31d587485976dfacbaa51e2bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358754"
---
# <a name="cbasewindowpaintwindow-method"></a><span data-ttu-id="e3886-103">Cbasewindow. paintwindow-Methode</span><span class="sxs-lookup"><span data-stu-id="e3886-103">CBaseWindow.PaintWindow method</span></span>

<span data-ttu-id="e3886-104">Die- `PaintWindow` Methode bewirkt, dass das Fenster neu gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="e3886-104">The `PaintWindow` method causes the window to be repainted.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3886-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3886-105">Syntax</span></span>


```C++
void PaintWindow(
   BOOL bErase
);
```



## <a name="parameters"></a><span data-ttu-id="e3886-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3886-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3886-107">*berase*</span><span class="sxs-lookup"><span data-stu-id="e3886-107">*bErase*</span></span> 
</dt> <dd>

<span data-ttu-id="e3886-108">Boolescher Wert, der angibt, ob der Hintergrund gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="e3886-108">Boolean value that specifies whether the background is erased.</span></span> <span data-ttu-id="e3886-109">Wenn der Wert **true** ist, wird der Hintergrund gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e3886-109">If the value is **TRUE**, the background is erased.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3886-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3886-110">Return value</span></span>

<span data-ttu-id="e3886-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e3886-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3886-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3886-112">Remarks</span></span>

<span data-ttu-id="e3886-113">Diese Methode generiert eine WM \_ -Zeichnungs Nachricht, indem der gesamte Client Bereich des Fensters ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="e3886-113">This method generates a WM\_PAINT message by invalidating the window's entire client area.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3886-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3886-114">Requirements</span></span>



| <span data-ttu-id="e3886-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3886-115">Requirement</span></span> | <span data-ttu-id="e3886-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e3886-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3886-117">Header</span><span class="sxs-lookup"><span data-stu-id="e3886-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e3886-118"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3886-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e3886-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e3886-119">Library</span></span><br/> | <dl> <span data-ttu-id="e3886-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e3886-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3886-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3886-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3886-122">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e3886-122">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




