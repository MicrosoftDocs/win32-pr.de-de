---
description: Die completeconnect-Methode benachrichtigt das Fenster, dass die Eingabe-PIN des Renderers verbunden wurde.
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: Cbasewindow. completeconnect-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 15d5719ab78c3e95cd0128d4075797221af1f4c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356352"
---
# <a name="cbasewindowcompleteconnect-method"></a><span data-ttu-id="78c1b-103">Cbasewindow. completeconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="78c1b-103">CBaseWindow.CompleteConnect method</span></span>

<span data-ttu-id="78c1b-104">Die `CompleteConnect` -Methode benachrichtigt das Fenster, dass die Eingabe-PIN des Renderers verbunden wurde.</span><span class="sxs-lookup"><span data-stu-id="78c1b-104">The `CompleteConnect` method notifies the window that the renderer's input pin has been connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="78c1b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="78c1b-105">Syntax</span></span>


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a><span data-ttu-id="78c1b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="78c1b-106">Parameters</span></span>

<span data-ttu-id="78c1b-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="78c1b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="78c1b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78c1b-108">Return value</span></span>

<span data-ttu-id="78c1b-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="78c1b-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="78c1b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78c1b-110">Remarks</span></span>

<span data-ttu-id="78c1b-111">Diese Methode setzt das Fenster Aktivierungs Flag ([**cbasewindow:: m \_ bactivated**](cbasewindow-m-bactivated.md)) auf **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="78c1b-111">This method resets the window activation flag ([**CBaseWindow::m\_bActivated**](cbasewindow-m-bactivated.md)) to **FALSE**.</span></span> <span data-ttu-id="78c1b-112">Wenn ein Videorenderer eine PIN-Verbindung abschließt, kann er die [**cbasewindow:: activatewindow**](cbasewindow-activatewindow.md) -Methode aufrufen, um die Größe und Position des Fensters festzulegen.</span><span class="sxs-lookup"><span data-stu-id="78c1b-112">When a video renderer completes a pin connection, it might call the [**CBaseWindow::ActivateWindow**](cbasewindow-activatewindow.md) method to set the window's size and position.</span></span> <span data-ttu-id="78c1b-113">Um die Neuberechnung dieser Attribute durch **activatewindow** zu erzwingen, müssen Sie zuerst die- `CompleteConnect` Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="78c1b-113">To force **ActivateWindow** to recalculate these attributes, first call the `CompleteConnect` method.</span></span>

## <a name="requirements"></a><span data-ttu-id="78c1b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78c1b-114">Requirements</span></span>



| <span data-ttu-id="78c1b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78c1b-115">Requirement</span></span> | <span data-ttu-id="78c1b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="78c1b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78c1b-117">Header</span><span class="sxs-lookup"><span data-stu-id="78c1b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="78c1b-118"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78c1b-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="78c1b-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="78c1b-119">Library</span></span><br/> | <dl> <span data-ttu-id="78c1b-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="78c1b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78c1b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78c1b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c1b-122">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="78c1b-122">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




