---
description: Die activatewindow-Methode passt das Fenster entsprechend den Anforderungen der abgeleiteten Klasse an.
ms.assetid: 39e23080-e4ae-46d5-bb3f-306c92bbfe14
title: Cbasewindow. activatewindow-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.ActivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f747f108bb6c7e42e90a0ff8503ec59a83c59699
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359677"
---
# <a name="cbasewindowactivatewindow-method"></a><span data-ttu-id="b8b56-103">Cbasewindow. activatewindow-Methode</span><span class="sxs-lookup"><span data-stu-id="b8b56-103">CBaseWindow.ActivateWindow method</span></span>

<span data-ttu-id="b8b56-104">Die- `ActivateWindow` Methode passt die Größe des Fensters gemäß den Anforderungen der abgeleiteten Klasse an.</span><span class="sxs-lookup"><span data-stu-id="b8b56-104">The `ActivateWindow` method sizes the window according to the requirements of the derived class.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8b56-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8b56-105">Syntax</span></span>


```C++
virtual HRESULT ActivateWindow();
```



## <a name="parameters"></a><span data-ttu-id="b8b56-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8b56-106">Parameters</span></span>

<span data-ttu-id="b8b56-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b8b56-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8b56-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8b56-108">Return value</span></span>

<span data-ttu-id="b8b56-109">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b8b56-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="b8b56-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b8b56-110">Return code</span></span>                                                                             | <span data-ttu-id="b8b56-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8b56-111">Description</span></span>                              |
|-----------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="b8b56-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b8b56-112"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="b8b56-113">Das Fenster wurde bereits aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b8b56-113">Window was already activated.</span></span><br/> |
| <dl> <span data-ttu-id="b8b56-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b8b56-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="b8b56-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="b8b56-115">Success.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="b8b56-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8b56-116">Remarks</span></span>

<span data-ttu-id="b8b56-117">Diese Methode ruft die [**cbasewindow:: getdefaultrect**](cbasewindow-getdefaultrect.md) -Methode auf, um die Fenstergröße zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="b8b56-117">This methods calls the [**CBaseWindow::GetDefaultRect**](cbasewindow-getdefaultrect.md) method to determine the window size.</span></span> <span data-ttu-id="b8b56-118">Die abgeleitete Klasse sollte **getdefaultrect** überschreiben, um die Größe der angezeigten Bilder zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="b8b56-118">The derived class should override **GetDefaultRect** to return the size of the images that will be displayed.</span></span>

<span data-ttu-id="b8b56-119">Wenn das Fenster bereits aktiv ist, wird `ActivateWindow` beim Aufrufen von das Fenster an den Anfang der Z-Reihenfolge verschoben, aber die Größe des Fensters wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="b8b56-119">If the window is already active, calling `ActivateWindow` moves the window to the top of the Z order, but does not resize the window.</span></span> <span data-ttu-id="b8b56-120">Das gleiche gilt, wenn das Fenster über ein übergeordnetes Element verfügt.</span><span class="sxs-lookup"><span data-stu-id="b8b56-120">The same is true if the window has a parent.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8b56-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8b56-121">Requirements</span></span>



| <span data-ttu-id="b8b56-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8b56-122">Requirement</span></span> | <span data-ttu-id="b8b56-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b8b56-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8b56-124">Header</span><span class="sxs-lookup"><span data-stu-id="b8b56-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b8b56-125"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8b56-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b8b56-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b8b56-126">Library</span></span><br/> | <dl> <span data-ttu-id="b8b56-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b8b56-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8b56-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8b56-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8b56-129">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b8b56-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




