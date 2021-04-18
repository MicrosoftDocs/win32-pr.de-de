---
description: Mit der get \_ windowstyleex-Methode werden die erweiterten Fenster Stile abgerufen.
ms.assetid: 72955958-bbda-4b8f-9c28-6d3f5eb56a82
title: CBaseControlWindow.get_WindowStyleEx-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c59336ab57e92e99366494a272f2b995191b494b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371740"
---
# <a name="cbasecontrolwindowget_windowstyleex-method"></a><span data-ttu-id="29101-103">Cbasecontrolwindow. get \_ windowstyleex-Methode</span><span class="sxs-lookup"><span data-stu-id="29101-103">CBaseControlWindow.get\_WindowStyleEx method</span></span>

<span data-ttu-id="29101-104">Die- `get_WindowStyleEx` Methode ruft die erweiterten Fenster Stile ab.</span><span class="sxs-lookup"><span data-stu-id="29101-104">The `get_WindowStyleEx` method retrieves the extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="29101-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="29101-105">Syntax</span></span>


```C++
HRESULT get_WindowStyleEx(
   long *pWindowStyleEx
);
```



## <a name="parameters"></a><span data-ttu-id="29101-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="29101-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29101-107">*pwindowstyleex*</span><span class="sxs-lookup"><span data-stu-id="29101-107">*pWindowStyleEx*</span></span> 
</dt> <dd>

<span data-ttu-id="29101-108">Zeiger auf Erweiterte Fenster Stile.</span><span class="sxs-lookup"><span data-stu-id="29101-108">Pointer to extended window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29101-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29101-109">Return value</span></span>

<span data-ttu-id="29101-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="29101-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29101-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29101-111">Remarks</span></span>

<span data-ttu-id="29101-112">Diese Member-Funktion Ruft die erweiterten Fenster Stile ab.</span><span class="sxs-lookup"><span data-stu-id="29101-112">This member function retrieves the extended window styles.</span></span> <span data-ttu-id="29101-113">Die [**cbasecontrolwindow::D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) -Member-Funktion wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="29101-113">It calls the [**CBaseControlWindow::DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md) member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="29101-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29101-114">Requirements</span></span>



| <span data-ttu-id="29101-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29101-115">Requirement</span></span> | <span data-ttu-id="29101-116">Wert</span><span class="sxs-lookup"><span data-stu-id="29101-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29101-117">Header</span><span class="sxs-lookup"><span data-stu-id="29101-117">Header</span></span><br/>  | <dl> <span data-ttu-id="29101-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29101-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="29101-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="29101-119">Library</span></span><br/> | <dl> <span data-ttu-id="29101-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="29101-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29101-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29101-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29101-122">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="29101-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




