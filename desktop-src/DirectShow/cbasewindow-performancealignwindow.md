---
description: Die performancealignwindow-Methode richtet die Fensterposition an DWORD-Begrenzungen aus, um eine maximale Leistung zu erzielen.
ms.assetid: e28950bc-2510-45b9-9c9c-c2a9dbc3dc02
title: Cbasewindow. performancealignwindow-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PerformanceAlignWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e6e7a54372743d430cd904f47c79414d149cf033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364449"
---
# <a name="cbasewindowperformancealignwindow-method"></a><span data-ttu-id="07425-103">Cbasewindow. performancealignwindow-Methode</span><span class="sxs-lookup"><span data-stu-id="07425-103">CBaseWindow.PerformanceAlignWindow method</span></span>

<span data-ttu-id="07425-104">Die- `PerformanceAlignWindow` Methode richtet die Fensterposition an **DWORD** -Begrenzungen aus, um eine maximale Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="07425-104">The `PerformanceAlignWindow` method aligns the window position to **DWORD** boundaries, for maximum performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="07425-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="07425-105">Syntax</span></span>


```C++
HRESULT PerformanceAlignWindow();
```



## <a name="parameters"></a><span data-ttu-id="07425-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="07425-106">Parameters</span></span>

<span data-ttu-id="07425-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="07425-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07425-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07425-108">Return value</span></span>

<span data-ttu-id="07425-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="07425-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="07425-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07425-110">Remarks</span></span>

<span data-ttu-id="07425-111">Diese Methode richtet den linken und oberen Rand des Fensters an DWORD-Begrenzungen aus, wodurch die Leistung verbessert werden kann.</span><span class="sxs-lookup"><span data-stu-id="07425-111">This method aligns the left and top edges of the window to DWORD boundaries, which can improve performance.</span></span> <span data-ttu-id="07425-112">Wenn das Fenster über ein übergeordnetes Element verfügt, gibt die Methode S OK zurück, führt \_ jedoch die Ausrichtung aus.</span><span class="sxs-lookup"><span data-stu-id="07425-112">If the window has a parent, the method returns S\_OK but does perform the alignment.</span></span>

## <a name="requirements"></a><span data-ttu-id="07425-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07425-113">Requirements</span></span>



| <span data-ttu-id="07425-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07425-114">Requirement</span></span> | <span data-ttu-id="07425-115">Wert</span><span class="sxs-lookup"><span data-stu-id="07425-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07425-116">Header</span><span class="sxs-lookup"><span data-stu-id="07425-116">Header</span></span><br/>  | <dl> <span data-ttu-id="07425-117"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07425-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="07425-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="07425-118">Library</span></span><br/> | <dl> <span data-ttu-id="07425-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="07425-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07425-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07425-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07425-121">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="07425-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




