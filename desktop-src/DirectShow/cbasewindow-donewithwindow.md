---
description: Die Methode "donewithwindow" zerstört das Fenster.
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: Cbasewindow. donewithwindow-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoneWithWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc31e893a4015aa8b4356d265ca4065ee336c3ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350795"
---
# <a name="cbasewindowdonewithwindow-method"></a><span data-ttu-id="b69d6-103">Cbasewindow. donewithwindow-Methode</span><span class="sxs-lookup"><span data-stu-id="b69d6-103">CBaseWindow.DoneWithWindow method</span></span>

<span data-ttu-id="b69d6-104">Die- `DoneWithWindow` Methode zerstört das-Fenster.</span><span class="sxs-lookup"><span data-stu-id="b69d6-104">The `DoneWithWindow` method destroys the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="b69d6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b69d6-105">Syntax</span></span>


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a><span data-ttu-id="b69d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b69d6-106">Parameters</span></span>

<span data-ttu-id="b69d6-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b69d6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b69d6-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b69d6-108">Return value</span></span>

<span data-ttu-id="b69d6-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="b69d6-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b69d6-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b69d6-110">Remarks</span></span>

<span data-ttu-id="b69d6-111">Ruft diese Methode aus der dekonstruktormethode des abgeleiteten Objekts auf.</span><span class="sxs-lookup"><span data-stu-id="b69d6-111">Call this method from the derived object's destructor method.</span></span>

<span data-ttu-id="b69d6-112">Wenn diese Methode vom gleichen Thread aufgerufen wird, der das Fenster erstellt hat, führt die-Methode die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="b69d6-112">If this method is called from the same thread that created the window, the method performs the following actions:</span></span>

-   <span data-ttu-id="b69d6-113">Ruft die [**cbasewindow:: inactivatewindow**](cbasewindow-inactivatewindow.md) -Methode auf, die das Fenster deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b69d6-113">Calls the [**CBaseWindow::InactivateWindow**](cbasewindow-inactivatewindow.md) method, which deactivates the window.</span></span>
-   <span data-ttu-id="b69d6-114">Ruft die [**cbasewindow:: uninitialisetwindow**](cbasewindow-uninitialisewindow.md) -Methode auf, die vom Fenster verwendete Ressourcen freigibt.</span><span class="sxs-lookup"><span data-stu-id="b69d6-114">Calls the [**CBaseWindow::UninitialiseWindow**](cbasewindow-uninitialisewindow.md) method, which releases resources used by the window.</span></span>
-   <span data-ttu-id="b69d6-115">Zerstört das Fenster.</span><span class="sxs-lookup"><span data-stu-id="b69d6-115">Destroys the window.</span></span>

<span data-ttu-id="b69d6-116">Wenn der aufrufenden Thread `DoneWithWindow` nicht der Thread ist, der das Fenster erstellt hat, sendet die Methode eine private "Destroy"-Meldung an das Fenster.</span><span class="sxs-lookup"><span data-stu-id="b69d6-116">If the thread calling `DoneWithWindow` is not the thread that created the window, the method sends a private "destroy" message to the window.</span></span> <span data-ttu-id="b69d6-117">Wenn das Fenster diese Nachricht empfängt, ruft es `DoneWithWindow` auf sich selbst auf.</span><span class="sxs-lookup"><span data-stu-id="b69d6-117">When the window receives this message, it calls `DoneWithWindow` on itself.</span></span> <span data-ttu-id="b69d6-118">(Wenn " [**cbasewindow:: m \_ bdopostdedestroy**](cbasewindow-m-bdoposttodestroy.md) " den Wert " **true**" hat, wird die Nachricht vom Fenster ausgegeben.)</span><span class="sxs-lookup"><span data-stu-id="b69d6-118">(If [**CBaseWindow::m\_bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) is **TRUE**, the window posts the message.)</span></span>

## <a name="requirements"></a><span data-ttu-id="b69d6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b69d6-119">Requirements</span></span>



| <span data-ttu-id="b69d6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b69d6-120">Requirement</span></span> | <span data-ttu-id="b69d6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b69d6-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b69d6-122">Header</span><span class="sxs-lookup"><span data-stu-id="b69d6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b69d6-123"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b69d6-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b69d6-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b69d6-124">Library</span></span><br/> | <dl> <span data-ttu-id="b69d6-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b69d6-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b69d6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b69d6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b69d6-127">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b69d6-127">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




