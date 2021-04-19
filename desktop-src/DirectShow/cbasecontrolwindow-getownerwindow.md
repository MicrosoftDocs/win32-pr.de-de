---
description: Die getownerwindow-Methode ruft das besitzende Fenster Handle "m \_ hwndOwner" ab.
ms.assetid: fa576b42-b4a7-4374-8ba4-7d21e86d9d61
title: Cbasecontrolwindow. getownerwindow-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetOwnerWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e4d3811f85abd68bcd7d625dce0e9e8963be39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369702"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a><span data-ttu-id="621a0-103">Cbasecontrolwindow. getownerwindow-Methode</span><span class="sxs-lookup"><span data-stu-id="621a0-103">CBaseControlWindow.GetOwnerWindow method</span></span>

<span data-ttu-id="621a0-104">Die- `GetOwnerWindow` Methode ruft das besitzende Fenster Handle " **m \_ hwndOwner**" ab.</span><span class="sxs-lookup"><span data-stu-id="621a0-104">The `GetOwnerWindow` method retrieves the owning window handle, **m\_hwndOwner**.</span></span>

## <a name="syntax"></a><span data-ttu-id="621a0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="621a0-105">Syntax</span></span>


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a><span data-ttu-id="621a0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="621a0-106">Parameters</span></span>

<span data-ttu-id="621a0-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="621a0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="621a0-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="621a0-108">Return value</span></span>

<span data-ttu-id="621a0-109">Gibt das Besitzer Fenster zurück.</span><span class="sxs-lookup"><span data-stu-id="621a0-109">Returns the owner window.</span></span>

## <a name="remarks"></a><span data-ttu-id="621a0-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="621a0-110">Remarks</span></span>

<span data-ttu-id="621a0-111">Ruft das besitzende Fenster ohne Aufrufen der Schnittstellen Methode ab.</span><span class="sxs-lookup"><span data-stu-id="621a0-111">Retrieves the owning window without calling the interface method.</span></span> <span data-ttu-id="621a0-112">Verwenden Sie diese Member-Funktion anstelle von " [**cbasecontrolwindow:: get \_ Owner**](cbasecontrolwindow-get-owner.md)", es sei denn, Sie rufen dies extern über die [**IVideoWindow:: get- \_ Besitzer**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) Methode auf.</span><span class="sxs-lookup"><span data-stu-id="621a0-112">Use this member function instead of [**CBaseControlWindow::get\_Owner**](cbasecontrolwindow-get-owner.md), unless you are calling this externally through the [**IVideoWindow::get\_Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="621a0-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="621a0-113">Requirements</span></span>



| <span data-ttu-id="621a0-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="621a0-114">Requirement</span></span> | <span data-ttu-id="621a0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="621a0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="621a0-116">Header</span><span class="sxs-lookup"><span data-stu-id="621a0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="621a0-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="621a0-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="621a0-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="621a0-118">Library</span></span><br/> | <dl> <span data-ttu-id="621a0-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="621a0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="621a0-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="621a0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="621a0-121">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="621a0-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




