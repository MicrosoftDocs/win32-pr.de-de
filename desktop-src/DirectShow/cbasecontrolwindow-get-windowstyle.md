---
description: Die get \_ Windows Style-Methode ruft die Standardfenster Stile ab.
ms.assetid: 5c204814-5c7c-47e2-95dd-86455ed77cc7
title: CBaseControlWindow.get_WindowStyle-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91e04efac3a67c262b4eeb85948f846dbb06086a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372707"
---
# <a name="cbasecontrolwindowget_windowstyle-method"></a><span data-ttu-id="3604d-103">Cbasecontrolwindow. get \_ WindowStyle-Methode</span><span class="sxs-lookup"><span data-stu-id="3604d-103">CBaseControlWindow.get\_WindowStyle method</span></span>

<span data-ttu-id="3604d-104">Die- `get_WindowStyle` Methode ruft die Standardfenster Stile ab.</span><span class="sxs-lookup"><span data-stu-id="3604d-104">The `get_WindowStyle` method retrieves the standard window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="3604d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3604d-105">Syntax</span></span>


```C++
HRESULT get_WindowStyle(
   long *pWindowStyle
);
```



## <a name="parameters"></a><span data-ttu-id="3604d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3604d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3604d-107">*pwindowstyle*</span><span class="sxs-lookup"><span data-stu-id="3604d-107">*pWindowStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="3604d-108">Zeiger auf Fenster Stile.</span><span class="sxs-lookup"><span data-stu-id="3604d-108">Pointer to window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3604d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3604d-109">Return value</span></span>

<span data-ttu-id="3604d-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3604d-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3604d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3604d-111">Remarks</span></span>

<span data-ttu-id="3604d-112">Diese Member-Funktion gibt die Standardfenster Stile zurück, wie z \_ . b. WS Child und WS \_ Visible.</span><span class="sxs-lookup"><span data-stu-id="3604d-112">This member function returns the standard window styles, such as WS\_CHILD and WS\_VISIBLE.</span></span> <span data-ttu-id="3604d-113">Die [**cbasecontrolwindow::D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) -Member-Funktion wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3604d-113">It calls the [**CBaseControlWindow::DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md) member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3604d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3604d-114">Requirements</span></span>



| <span data-ttu-id="3604d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3604d-115">Requirement</span></span> | <span data-ttu-id="3604d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3604d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3604d-117">Header</span><span class="sxs-lookup"><span data-stu-id="3604d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3604d-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3604d-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3604d-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3604d-119">Library</span></span><br/> | <dl> <span data-ttu-id="3604d-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3604d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3604d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3604d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3604d-122">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3604d-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




