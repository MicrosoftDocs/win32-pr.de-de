---
description: Die get \_ AutoShow-Methode ruft das aktuelle Autoshow State-Flag ab.
ms.assetid: b27651d1-3ac5-4a52-9549-b63bacda5dc8
title: CBaseControlWindow.get_AutoShow-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f45679b9d036f1c5386cd2c1d18a31fa3d6bd64f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372253"
---
# <a name="cbasecontrolwindowget_autoshow-method"></a><span data-ttu-id="9f6a6-103">Cbasecontrolwindow. get \_ AutoShow-Methode</span><span class="sxs-lookup"><span data-stu-id="9f6a6-103">CBaseControlWindow.get\_AutoShow method</span></span>

<span data-ttu-id="9f6a6-104">Die- `get_AutoShow` Methode ruft das aktuelle Autoshow State-Flag ab.</span><span class="sxs-lookup"><span data-stu-id="9f6a6-104">The `get_AutoShow` method retrieves the current AutoShow state flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f6a6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f6a6-105">Syntax</span></span>


```C++
HRESULT get_AutoShow(
   long *AutoShow
);
```



## <a name="parameters"></a><span data-ttu-id="9f6a6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f6a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f6a6-107">*Automatisch anzeigen*</span><span class="sxs-lookup"><span data-stu-id="9f6a6-107">*AutoShow*</span></span> 
</dt> <dd>

<span data-ttu-id="9f6a6-108">Zeiger auf ein boolesches Automatisierungs Flag (0 ist off, 1 ist on).</span><span class="sxs-lookup"><span data-stu-id="9f6a6-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f6a6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f6a6-109">Return value</span></span>

<span data-ttu-id="9f6a6-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9f6a6-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f6a6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f6a6-111">Remarks</span></span>

<span data-ttu-id="9f6a6-112">Diese Member-Funktion implementiert die [**IVideoWindow:: get \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9f6a6-112">This member function implements the [**IVideoWindow::get\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) method.</span></span> <span data-ttu-id="9f6a6-113">Diese Eigenschaft vereinfacht den Fenster Anzeige Zugriff für-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="9f6a6-113">This property simplifies window display access for applications.</span></span> <span data-ttu-id="9f6a6-114">Wenn dieser Wert auf 1 (on) festgelegt ist, wird das Fenster, das in der Regel nach der Verbindungs Herstellung ausgeblendet wird, automatisch angezeigt, wenn der Filter anhält oder ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f6a6-114">If this is set to  1 (on), the window, which is typically hidden after connection of the filter, will be displayed automatically when the filter pauses or runs.</span></span> <span data-ttu-id="9f6a6-115">Das Fenster sollte jedoch nicht ausgeblendet werden, wenn der Filter angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="9f6a6-115">The window should not be hidden when the filter stops, however.</span></span> <span data-ttu-id="9f6a6-116">Wenn dieser Parameter auf 0 (Off) festgelegt ist, wird das Fenster nur angezeigt, wenn die Anwendung [**cbasecontrolwindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) oder [**cbasecontrolwindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) mit den entsprechenden Parametern aufruft.</span><span class="sxs-lookup"><span data-stu-id="9f6a6-116">If this parameter is set to 0 (off), the window is made visible only when the application calls [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) with the appropriate parameters.</span></span>

<span data-ttu-id="9f6a6-117">Diese Member-Funktion soll von externen Objekten über die [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle aufgerufen werden und sperrt daher den kritischen Abschnitt, um mit dem zugeordneten Filter synchronisiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="9f6a6-117">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="9f6a6-118">Rufen Sie die Member-Funktion [**cbasecontrolwindow:: isautoshowenabled**](cbasecontrolwindow-isautoshowenabled.md) auf, um diese Eigenschaft abzurufen, wenn Sie nicht von einem externen Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9f6a6-118">Call the [**CBaseControlWindow::IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) member function to retrieve this property if you are not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f6a6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f6a6-119">Requirements</span></span>



| <span data-ttu-id="9f6a6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f6a6-120">Requirement</span></span> | <span data-ttu-id="9f6a6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9f6a6-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f6a6-122">Header</span><span class="sxs-lookup"><span data-stu-id="9f6a6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9f6a6-123"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f6a6-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9f6a6-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9f6a6-124">Library</span></span><br/> | <dl> <span data-ttu-id="9f6a6-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9f6a6-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f6a6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f6a6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f6a6-127">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9f6a6-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




