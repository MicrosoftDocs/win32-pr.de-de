---
description: Die OnClose-Methode behandelt WM- \_ Schließen-Nachrichten.
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: Cbasewindow. OnClose-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnClose
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 189b08c116f66ff864ffe308befb990973c6ce43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369991"
---
# <a name="cbasewindowonclose-method"></a><span data-ttu-id="26a59-103">Cbasewindow. OnClose-Methode</span><span class="sxs-lookup"><span data-stu-id="26a59-103">CBaseWindow.OnClose method</span></span>

<span data-ttu-id="26a59-104">Die- `OnClose` Methode behandelt WM- \_ Schließen-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="26a59-104">The `OnClose` method handles WM\_CLOSE messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="26a59-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="26a59-105">Syntax</span></span>


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a><span data-ttu-id="26a59-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="26a59-106">Parameters</span></span>

<span data-ttu-id="26a59-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="26a59-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26a59-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26a59-108">Return value</span></span>

<span data-ttu-id="26a59-109">Gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="26a59-109">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="26a59-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26a59-110">Remarks</span></span>

<span data-ttu-id="26a59-111">In der Basisklasse blendet diese Methode einfach das Fenster aus.</span><span class="sxs-lookup"><span data-stu-id="26a59-111">In the base class, this method simply hides the window.</span></span> <span data-ttu-id="26a59-112">In der Regel wird diese Methode von einer abgeleiteten Klasse überschrieben, sodass auch ein [**EC \_ userabort**](ec-userabort.md) -Ereignis gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="26a59-112">Typically, a derived class will override this method so that it sends an [**EC\_USERABORT**](ec-userabort.md) event as well.</span></span> <span data-ttu-id="26a59-113">Überschreiben Sie die-Methode nicht, um das Fenster zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="26a59-113">Do not override the method to destroy the window.</span></span> <span data-ttu-id="26a59-114">Stattdessen wird die Methode [**cbasewindow::D onewithwindow**](cbasewindow-donewithwindow.md) aufgerufen, wenn der besitzende Filter zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="26a59-114">Instead, call the [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method when the owning filter is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="26a59-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26a59-115">Requirements</span></span>



| <span data-ttu-id="26a59-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26a59-116">Requirement</span></span> | <span data-ttu-id="26a59-117">Wert</span><span class="sxs-lookup"><span data-stu-id="26a59-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26a59-118">Header</span><span class="sxs-lookup"><span data-stu-id="26a59-118">Header</span></span><br/>  | <dl> <span data-ttu-id="26a59-119"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26a59-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="26a59-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="26a59-120">Library</span></span><br/> | <dl> <span data-ttu-id="26a59-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="26a59-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26a59-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26a59-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26a59-123">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="26a59-123">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




