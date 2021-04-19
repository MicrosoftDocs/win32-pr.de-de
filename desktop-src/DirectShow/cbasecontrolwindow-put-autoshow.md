---
description: Die Put \_ AutoShow-Methode legt das Autoshow State-Flag fest.
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: CBaseControlWindow.put_AutoShow-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda5c0c4055979537c5cc471053715e29a348f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359332"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a><span data-ttu-id="930e9-103">Cbasecontrolwindow. Put \_ AutoShow-Methode</span><span class="sxs-lookup"><span data-stu-id="930e9-103">CBaseControlWindow.put\_AutoShow method</span></span>

<span data-ttu-id="930e9-104">Die- `put_AutoShow` Methode legt das Autoshow State-Flag fest.</span><span class="sxs-lookup"><span data-stu-id="930e9-104">The `put_AutoShow` method sets the AutoShow state flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="930e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="930e9-105">Syntax</span></span>


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a><span data-ttu-id="930e9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="930e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="930e9-107">*Automatisch anzeigen*</span><span class="sxs-lookup"><span data-stu-id="930e9-107">*AutoShow*</span></span> 
</dt> <dd>

<span data-ttu-id="930e9-108">Boolesches Automatisierungs Flag (0 ist off, 1 ist on).</span><span class="sxs-lookup"><span data-stu-id="930e9-108">Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="930e9-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="930e9-109">Return value</span></span>

<span data-ttu-id="930e9-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="930e9-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="930e9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="930e9-111">Remarks</span></span>

<span data-ttu-id="930e9-112">Diese Eigenschaft vereinfacht den Fenster Anzeige Zugriff für-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="930e9-112">This property simplifies window display access for applications.</span></span> <span data-ttu-id="930e9-113">Wenn dieser Wert auf 1 (on) festgelegt ist, wird das Fenster, das in der Regel ausgeblendet wird, nachdem der Filter verbunden ist, automatisch angezeigt, wenn der Filter anhält oder ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="930e9-113">If this is set to  1 (on), the window, which is typically hidden after the filter is connected, will be displayed automatically when the filter pauses or runs.</span></span> <span data-ttu-id="930e9-114">Das Fenster sollte jedoch nicht ausgeblendet werden, wenn der Filter angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="930e9-114">The window should not be hidden when the filter stops, however.</span></span> <span data-ttu-id="930e9-115">Wenn dieser Wert auf 0 (Off) festgelegt ist, wird das Fenster nur dann sichtbar, wenn die Anwendung [**cbasecontrolwindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) oder [**cbasecontrolwindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) mit den entsprechenden Parametern aufruft.</span><span class="sxs-lookup"><span data-stu-id="930e9-115">If this is set to 0 (off), the window is made visible only when the application calls [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) with the appropriate parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="930e9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="930e9-116">Requirements</span></span>



| <span data-ttu-id="930e9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="930e9-117">Requirement</span></span> | <span data-ttu-id="930e9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="930e9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="930e9-119">Header</span><span class="sxs-lookup"><span data-stu-id="930e9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="930e9-120"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="930e9-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="930e9-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="930e9-121">Library</span></span><br/> | <dl> <span data-ttu-id="930e9-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="930e9-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="930e9-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="930e9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="930e9-124">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="930e9-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




