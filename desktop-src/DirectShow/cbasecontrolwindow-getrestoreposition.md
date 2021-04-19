---
description: Die getrestoreposition-Methode ruft die Position ab, an der das Fenster wieder hergestellt wird, wenn es nicht maximiert oder minimiert wird.
ms.assetid: 5f129be3-c4d8-4583-bbc8-870e0bcafd80
title: Cbasecontrolwindow. getrestoreposition-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetRestorePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f922a97f69f4dae03d4e61a54bd99c52d69a984a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372049"
---
# <a name="cbasecontrolwindowgetrestoreposition-method"></a><span data-ttu-id="f3604-103">Cbasecontrolwindow. getrestoreposition-Methode</span><span class="sxs-lookup"><span data-stu-id="f3604-103">CBaseControlWindow.GetRestorePosition method</span></span>

<span data-ttu-id="f3604-104">Die- `GetRestorePosition` Methode ruft die Position ab, an der das Fenster wieder hergestellt wird, wenn es nicht maximiert oder minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="f3604-104">The `GetRestorePosition` method retrieves the position to which the window will be restored when it is not maximized or minimized.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3604-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3604-105">Syntax</span></span>


```C++
HRESULT GetRestorePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="f3604-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3604-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3604-107">*pleft*</span><span class="sxs-lookup"><span data-stu-id="f3604-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="f3604-108">Zeiger auf den Wert für die äußteste linke Koordinate.</span><span class="sxs-lookup"><span data-stu-id="f3604-108">Pointer to the value for leftmost coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="f3604-109">*ptop*</span><span class="sxs-lookup"><span data-stu-id="f3604-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="f3604-110">Zeiger auf den Wert für den oberen Rand des Fensters.</span><span class="sxs-lookup"><span data-stu-id="f3604-110">Pointer to the value for top of the window.</span></span>

</dd> <dt>

<span data-ttu-id="f3604-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="f3604-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="f3604-112">Zeiger auf den Wert für die Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="f3604-112">Pointer to the value for width of the window.</span></span>

</dd> <dt>

<span data-ttu-id="f3604-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="f3604-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="f3604-114">Zeiger auf den Wert für die Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="f3604-114">Pointer to the value for height of window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3604-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3604-115">Return value</span></span>

<span data-ttu-id="f3604-116">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f3604-116">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3604-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3604-117">Remarks</span></span>

<span data-ttu-id="f3604-118">Dies entspricht den Werten, die von der [**cbasecontrolwindow:: getwindowposition**](cbasecontrolwindow-getwindowposition.md) -Funktion zurückgegeben werden, wenn das Fenster weder maximiert noch minimiert ist.</span><span class="sxs-lookup"><span data-stu-id="f3604-118">This is the same as the values returned by the [**CBaseControlWindow::GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) function when the window is neither maximized nor minimized.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3604-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3604-119">Requirements</span></span>



| <span data-ttu-id="f3604-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3604-120">Requirement</span></span> | <span data-ttu-id="f3604-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f3604-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3604-122">Header</span><span class="sxs-lookup"><span data-stu-id="f3604-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f3604-123"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3604-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f3604-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f3604-124">Library</span></span><br/> | <dl> <span data-ttu-id="f3604-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f3604-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3604-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3604-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3604-127">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f3604-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




