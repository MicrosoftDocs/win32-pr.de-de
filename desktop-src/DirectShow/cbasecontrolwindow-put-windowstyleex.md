---
description: Mit der Put \_ windowstyleex-Methode werden die erweiterten Fenster Stile festgelegt.
ms.assetid: 3c5928fe-7cd3-4e1c-9a3f-fa6d7a73dbc3
title: CBaseControlWindow.put_WindowStyleEx-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee04cf2d2b2dcaafdaf4e989fd1118abf447698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364482"
---
# <a name="cbasecontrolwindowput_windowstyleex-method"></a><span data-ttu-id="14268-103">Cbasecontrolwindow. Put \_ windowstyleex-Methode</span><span class="sxs-lookup"><span data-stu-id="14268-103">CBaseControlWindow.put\_WindowStyleEx method</span></span>

<span data-ttu-id="14268-104">Die- `put_WindowStyleEx` Methode legt die erweiterten Fenster Stile fest.</span><span class="sxs-lookup"><span data-stu-id="14268-104">The `put_WindowStyleEx` method sets the extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="14268-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14268-105">Syntax</span></span>


```C++
HRESULT put_WindowStyleEx(
  [in] long WindowStyleEx
);
```



## <a name="parameters"></a><span data-ttu-id="14268-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14268-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14268-107">*Windowstyleex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14268-107">*WindowStyleEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14268-108">Ein-Wert, der den Stil des Steuerelement Fensters angibt.</span><span class="sxs-lookup"><span data-stu-id="14268-108">Value that specifies the style of the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14268-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14268-109">Return value</span></span>

<span data-ttu-id="14268-110">Gibt noError zurück.</span><span class="sxs-lookup"><span data-stu-id="14268-110">Returns NOERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="14268-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14268-111">Remarks</span></span>

<span data-ttu-id="14268-112">Diese Methode verwendet erweiterte Fenster Stile.</span><span class="sxs-lookup"><span data-stu-id="14268-112">This method uses extended window styles.</span></span> <span data-ttu-id="14268-113">Eine umfassende Liste der erweiterten Fenster Stile finden Sie in der **Microsoft Win32-** Funktion "Microsoft-Win32-Funktion".</span><span class="sxs-lookup"><span data-stu-id="14268-113">For a complete list of extended window styles, see the Microsoft Win32 **CreateWindowEx** function.</span></span> <span data-ttu-id="14268-114">Um den Fenster Stil zu ändern, rufen Sie den aktuellen Fenster Stil ab, und fügen Sie dann die erforderlichen Bitfelder hinzu, oder entfernen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="14268-114">To change the window style, retrieve the current window style, and then add or remove the necessary bit fields.</span></span>

<span data-ttu-id="14268-115">Verwenden Sie die folgenden Fenster Stile nicht, da Sie nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="14268-115">Do not use the following window styles because they are not validated.</span></span>

-   <span data-ttu-id="14268-116">WS \_ deaktiviert</span><span class="sxs-lookup"><span data-stu-id="14268-116">WS\_DISABLED</span></span>
-   <span data-ttu-id="14268-117">WS \_ HScroll</span><span class="sxs-lookup"><span data-stu-id="14268-117">WS\_HSCROLL</span></span>
-   <span data-ttu-id="14268-118">WS \_ -Symbol</span><span class="sxs-lookup"><span data-stu-id="14268-118">WS\_ICONIC</span></span>
-   <span data-ttu-id="14268-119">WS- \_ Maximierung</span><span class="sxs-lookup"><span data-stu-id="14268-119">WS\_MAXIMIZE</span></span>
-   <span data-ttu-id="14268-120">WS- \_ Minimierung</span><span class="sxs-lookup"><span data-stu-id="14268-120">WS\_MINIMIZE</span></span>
-   <span data-ttu-id="14268-121">WS- \_ VScroll</span><span class="sxs-lookup"><span data-stu-id="14268-121">WS\_VSCROLL</span></span>

<span data-ttu-id="14268-122">Mit einigen Ausnahmen (Beachten Sie hier) sind die zulässigen Flags identisch mit denen, die von der Win32-Funktion "up **Window** " zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="14268-122">With some exceptions (noted here), the acceptable flags are the same as those allowed by the Win32 **CreateWindow** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="14268-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14268-123">Requirements</span></span>



| <span data-ttu-id="14268-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14268-124">Requirement</span></span> | <span data-ttu-id="14268-125">Wert</span><span class="sxs-lookup"><span data-stu-id="14268-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14268-126">Header</span><span class="sxs-lookup"><span data-stu-id="14268-126">Header</span></span><br/>  | <dl> <span data-ttu-id="14268-127"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14268-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="14268-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="14268-128">Library</span></span><br/> | <dl> <span data-ttu-id="14268-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="14268-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14268-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14268-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14268-131">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="14268-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




