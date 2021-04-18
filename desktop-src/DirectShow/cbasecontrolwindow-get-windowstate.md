---
description: Die get \_ WindowState-Methode ruft den aktuellen Fenster Zustand ab.
ms.assetid: 118b6710-b041-4a7d-8cdb-b96ae3dcbb09
title: CBaseControlWindow.get_WindowState-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5391a118e2ae860a37905c7ff94822ad7c422135
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371515"
---
# <a name="cbasecontrolwindowget_windowstate-method"></a><span data-ttu-id="796e5-103">Cbasecontrolwindow. get \_ WindowState-Methode</span><span class="sxs-lookup"><span data-stu-id="796e5-103">CBaseControlWindow.get\_WindowState method</span></span>

<span data-ttu-id="796e5-104">Die- `get_WindowState` Methode ruft den aktuellen Fenster Zustand ab.</span><span class="sxs-lookup"><span data-stu-id="796e5-104">The `get_WindowState` method retrieves the current window state.</span></span>

## <a name="syntax"></a><span data-ttu-id="796e5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="796e5-105">Syntax</span></span>


```C++
HRESULT get_WindowState(
   long *pWindowState
);
```



## <a name="parameters"></a><span data-ttu-id="796e5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="796e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="796e5-107">*pwindowstate*</span><span class="sxs-lookup"><span data-stu-id="796e5-107">*pWindowState*</span></span> 
</dt> <dd>

<span data-ttu-id="796e5-108">Zeiger auf den Fenster Zustand.</span><span class="sxs-lookup"><span data-stu-id="796e5-108">Pointer to the window state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="796e5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="796e5-109">Return value</span></span>

<span data-ttu-id="796e5-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="796e5-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="796e5-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="796e5-111">Remarks</span></span>

<span data-ttu-id="796e5-112">Diese Member-Funktion gibt eine Teilmenge der Parameter der Microsoft Win32 **ShowWindow** -Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="796e5-112">This member function returns a subset of the parameters of the Microsoft Win32 **ShowWindow** function.</span></span> <span data-ttu-id="796e5-113">Vor allem gibt Sie in \_ \_ Abhängigkeit von der aktuellen Sichtbarkeit des Fensters "SW Show" und "SW Hide" zurück.</span><span class="sxs-lookup"><span data-stu-id="796e5-113">In particular, it returns SW\_SHOW and SW\_HIDE, depending on the current visibility of the window.</span></span> <span data-ttu-id="796e5-114">Außerdem gibt es eine "SW \_ -minimieren" und "SW \_ maximieren" zurück, je nachdem, ob das Fenster ein Symbol ist oder erweitert</span><span class="sxs-lookup"><span data-stu-id="796e5-114">It also returns SW\_MINIMIZE and SW\_MAXIMIZE, depending on whether the window is an icon or is expanded.</span></span>

## <a name="requirements"></a><span data-ttu-id="796e5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="796e5-115">Requirements</span></span>



| <span data-ttu-id="796e5-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="796e5-116">Requirement</span></span> | <span data-ttu-id="796e5-117">Wert</span><span class="sxs-lookup"><span data-stu-id="796e5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="796e5-118">Header</span><span class="sxs-lookup"><span data-stu-id="796e5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="796e5-119"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="796e5-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="796e5-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="796e5-120">Library</span></span><br/> | <dl> <span data-ttu-id="796e5-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="796e5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="796e5-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="796e5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="796e5-123">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="796e5-123">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




