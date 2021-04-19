---
description: Die onreceivemess Age-Methode verarbeitet Fenster Meldungen.
ms.assetid: 0f074f9b-00e5-42ff-a491-020d441acad1
title: Cbasewindow. onreceivemess Age-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: defef9a7ca24d6875eda508989615f308a2385b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366927"
---
# <a name="cbasewindowonreceivemessage-method"></a><span data-ttu-id="03310-103">Cbasewindow. onreceivemess Age-Methode</span><span class="sxs-lookup"><span data-stu-id="03310-103">CBaseWindow.OnReceiveMessage method</span></span>

<span data-ttu-id="03310-104">Die- `OnReceiveMessage` Methode verarbeitet Fenster Meldungen.</span><span class="sxs-lookup"><span data-stu-id="03310-104">The `OnReceiveMessage` method handles window messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="03310-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="03310-105">Syntax</span></span>


```C++
virtual LRESULT OnReceiveMessage(
   HWND   hwnd,
   INT    uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="03310-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="03310-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03310-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="03310-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="03310-108">Handle für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="03310-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="03310-109">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="03310-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="03310-110">Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="03310-110">Message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="03310-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03310-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03310-112">Der erste Message-Parameter.</span><span class="sxs-lookup"><span data-stu-id="03310-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="03310-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03310-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03310-114">Der zweite Meldungs Parameter.</span><span class="sxs-lookup"><span data-stu-id="03310-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03310-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03310-115">Return value</span></span>

<span data-ttu-id="03310-116">Gibt 0 zurück, wenn die Meldung verarbeitet wurde, oder 1, wenn die Meldung nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="03310-116">Returns 0 if the message was processed, or 1 if the message was not processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="03310-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03310-117">Remarks</span></span>

<span data-ttu-id="03310-118">Die-Basisklasse verarbeitet die folgenden Meldungen:</span><span class="sxs-lookup"><span data-stu-id="03310-118">The base class handles the following messages:</span></span>

-   <span data-ttu-id="03310-119">WM \_ Schließen</span><span class="sxs-lookup"><span data-stu-id="03310-119">WM\_CLOSE</span></span>
-   <span data-ttu-id="03310-120">WM \_ verschieben</span><span class="sxs-lookup"><span data-stu-id="03310-120">WM\_MOVE</span></span>
-   <span data-ttu-id="03310-121">WM \_ palettechanged</span><span class="sxs-lookup"><span data-stu-id="03310-121">WM\_PALETTECHANGED</span></span>
-   <span data-ttu-id="03310-122">WM \_ querynewpalette</span><span class="sxs-lookup"><span data-stu-id="03310-122">WM\_QUERYNEWPALETTE</span></span>
-   <span data-ttu-id="03310-123">WM- \_ Größe</span><span class="sxs-lookup"><span data-stu-id="03310-123">WM\_SIZE</span></span>
-   <span data-ttu-id="03310-124">WM- \_ syscolorchange</span><span class="sxs-lookup"><span data-stu-id="03310-124">WM\_SYSCOLORCHANGE</span></span>

<span data-ttu-id="03310-125">Eine abgeleitete Klasse kann diese Methode überschreiben, um andere Nachrichten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="03310-125">A derived class can override this method to handle other messages.</span></span> <span data-ttu-id="03310-126">Die abgeleitete Klasse sollte die Basisklassen Methode zum Verarbeiten von Nachrichten, die von der abgeleiteten Klasse ignoriert werden, aufruft.</span><span class="sxs-lookup"><span data-stu-id="03310-126">The derived class should call the base class method to handle any messages that the derived class ignores.</span></span>

## <a name="requirements"></a><span data-ttu-id="03310-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03310-127">Requirements</span></span>



| <span data-ttu-id="03310-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03310-128">Requirement</span></span> | <span data-ttu-id="03310-129">Wert</span><span class="sxs-lookup"><span data-stu-id="03310-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03310-130">Header</span><span class="sxs-lookup"><span data-stu-id="03310-130">Header</span></span><br/>  | <dl> <span data-ttu-id="03310-131"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03310-131"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="03310-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="03310-132">Library</span></span><br/> | <dl> <span data-ttu-id="03310-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="03310-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03310-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03310-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03310-135">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="03310-135">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




