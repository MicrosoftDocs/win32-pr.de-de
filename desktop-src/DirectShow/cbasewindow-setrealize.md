---
description: Die Methode "Methode" gibt an, ob im Fenster Paletten realisiert werden.
ms.assetid: ab4a6069-c11f-4126-93bf-6de5277970a1
title: Cbasewindow. ontrealize-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetRealize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 587e54cdbbbf57ddb4cf52e2d5dfb916acaee22d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361057"
---
# <a name="cbasewindowsetrealize-method"></a><span data-ttu-id="654f0-103">Cbasewindow. abtrealize-Methode</span><span class="sxs-lookup"><span data-stu-id="654f0-103">CBaseWindow.SetRealize method</span></span>

<span data-ttu-id="654f0-104">Die- `SetRealize` Methode gibt an, ob im Fenster Paletten realisiert werden.</span><span class="sxs-lookup"><span data-stu-id="654f0-104">The `SetRealize` method specifies whether the window realizes palettes.</span></span>

## <a name="syntax"></a><span data-ttu-id="654f0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="654f0-105">Syntax</span></span>


```C++
void SetRealize(
   BOOL bRealize
);
```



## <a name="parameters"></a><span data-ttu-id="654f0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="654f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="654f0-107">*zu brealisieren*</span><span class="sxs-lookup"><span data-stu-id="654f0-107">*bRealize*</span></span> 
</dt> <dd>

<span data-ttu-id="654f0-108">Boolescher Wert, der angibt, ob Paletten erkannt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="654f0-108">Boolean value that specifies whether to realize palettes.</span></span> <span data-ttu-id="654f0-109">**True** gibt an, dass die [**cbasewindow:: SetPalette**](cbasewindow-setpalette.md) -Methode Paletten erkennt.</span><span class="sxs-lookup"><span data-stu-id="654f0-109">If **TRUE**, the [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) method realizes palettes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="654f0-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="654f0-110">Return value</span></span>

<span data-ttu-id="654f0-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="654f0-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="654f0-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="654f0-112">Remarks</span></span>

<span data-ttu-id="654f0-113">Standardmäßig erkennt die **SetPalette** -Methode die angegebene Palette.</span><span class="sxs-lookup"><span data-stu-id="654f0-113">By default, the **SetPalette** method realizes the specified palette.</span></span> <span data-ttu-id="654f0-114">Diese Methode wird aufgerufen, um das Standardverhalten zu ändern, sodass die Paletten ausgewählt, aber nicht realisiert werden.</span><span class="sxs-lookup"><span data-stu-id="654f0-114">Call this method to change the default behavior, so that palettes are selected but not realized.</span></span> <span data-ttu-id="654f0-115">Diese Methode legt die Element Variable [**cbasewindow:: m \_ bnorealize**](cbasewindow-m-bnorealize.md) fest.</span><span class="sxs-lookup"><span data-stu-id="654f0-115">This method sets the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="654f0-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="654f0-116">Requirements</span></span>



| <span data-ttu-id="654f0-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="654f0-117">Requirement</span></span> | <span data-ttu-id="654f0-118">Wert</span><span class="sxs-lookup"><span data-stu-id="654f0-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="654f0-119">Header</span><span class="sxs-lookup"><span data-stu-id="654f0-119">Header</span></span><br/>  | <dl> <span data-ttu-id="654f0-120"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="654f0-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="654f0-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="654f0-121">Library</span></span><br/> | <dl> <span data-ttu-id="654f0-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="654f0-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="654f0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="654f0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="654f0-124">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="654f0-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




