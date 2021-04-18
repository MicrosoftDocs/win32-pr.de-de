---
description: Mit der Put \_ WindowState-Methode wird der Fenster Zustand festgelegt.
ms.assetid: 0d22fa84-17bc-4228-b86e-d31857156802
title: CBaseControlWindow.put_WindowState-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1944e9bd39816cd1f022296b69fdac60d0779f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358141"
---
# <a name="cbasecontrolwindowput_windowstate-method"></a><span data-ttu-id="d66a7-103">Cbasecontrolwindow. Put \_ WindowState-Methode</span><span class="sxs-lookup"><span data-stu-id="d66a7-103">CBaseControlWindow.put\_WindowState method</span></span>

<span data-ttu-id="d66a7-104">Die- `put_WindowState` Methode legt den Fenster Zustand fest.</span><span class="sxs-lookup"><span data-stu-id="d66a7-104">The `put_WindowState` method sets the window state.</span></span>

## <a name="syntax"></a><span data-ttu-id="d66a7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d66a7-105">Syntax</span></span>


```C++
HRESULT put_WindowState(
   long WindowState
);
```



## <a name="parameters"></a><span data-ttu-id="d66a7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d66a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d66a7-107">*WindowState*</span><span class="sxs-lookup"><span data-stu-id="d66a7-107">*WindowState*</span></span> 
</dt> <dd>

<span data-ttu-id="d66a7-108">Neuer Fenster Zustand.</span><span class="sxs-lookup"><span data-stu-id="d66a7-108">New window state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d66a7-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d66a7-109">Return value</span></span>

<span data-ttu-id="d66a7-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d66a7-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d66a7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d66a7-111">Remarks</span></span>

<span data-ttu-id="d66a7-112">Diese Member-Funktion nimmt dieselben Parameter wie die Microsoft Win32 **ShowWindow** -Funktion (z. b. WS \_ shownormal, WS \_ showminnoaktivierungs und WS \_ showmaximized).</span><span class="sxs-lookup"><span data-stu-id="d66a7-112">This member function takes the same parameters as the Microsoft Win32 **ShowWindow** function (for example, WS\_SHOWNORMAL, WS\_SHOWMINNOACTIVATE, and WS\_SHOWMAXIMIZED).</span></span>

## <a name="requirements"></a><span data-ttu-id="d66a7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d66a7-113">Requirements</span></span>



| <span data-ttu-id="d66a7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d66a7-114">Requirement</span></span> | <span data-ttu-id="d66a7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d66a7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d66a7-116">Header</span><span class="sxs-lookup"><span data-stu-id="d66a7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d66a7-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d66a7-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d66a7-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d66a7-118">Library</span></span><br/> | <dl> <span data-ttu-id="d66a7-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d66a7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d66a7-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d66a7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d66a7-121">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d66a7-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




