---
description: Mit der possiblyeatmessage-Methode kann eine abgeleitete Klasse Nachrichten an ein anderes Fenster weiterleiten.
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: Cbasewindow. possiblyeatmessage-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f218b62ac5464da27b8596992c34ce7ae5efde46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365968"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a><span data-ttu-id="0f8a7-103">Cbasewindow. possiblyeatmessage-Methode</span><span class="sxs-lookup"><span data-stu-id="0f8a7-103">CBaseWindow.PossiblyEatMessage method</span></span>

<span data-ttu-id="0f8a7-104">Mit der- `PossiblyEatMessage` Methode kann eine abgeleitete Klasse Nachrichten an ein anderes Fenster weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="0f8a7-104">The `PossiblyEatMessage` method enables a derived class to forward messages to another window.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f8a7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f8a7-105">Syntax</span></span>


```C++
virtual BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="0f8a7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f8a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f8a7-107">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="0f8a7-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="0f8a7-108">Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="0f8a7-108">Message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0f8a7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f8a7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f8a7-110">Der erste Message-Parameter.</span><span class="sxs-lookup"><span data-stu-id="0f8a7-110">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0f8a7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f8a7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f8a7-112">Der zweite Meldungs Parameter.</span><span class="sxs-lookup"><span data-stu-id="0f8a7-112">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f8a7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f8a7-113">Return value</span></span>

<span data-ttu-id="0f8a7-114">Gibt **true** zurück, wenn die Nachricht weitergeleitet wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="0f8a7-114">Returns **TRUE** if the message was forwarded, or **FALSE** otherwise.</span></span> <span data-ttu-id="0f8a7-115">Die Basisklasse gibt **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="0f8a7-115">The base class returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f8a7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f8a7-116">Remarks</span></span>

<span data-ttu-id="0f8a7-117">Bevor die [**cbasewindow:: onreceivemess**](cbasewindow-onreceivemessage.md) -Methode eine Nachricht verarbeitet, ruft Sie auf `PossiblyEatMessage` .</span><span class="sxs-lookup"><span data-stu-id="0f8a7-117">Before the [**CBaseWindow::OnReceiveMessage**](cbasewindow-onreceivemessage.md) method handles a message, it calls `PossiblyEatMessage`.</span></span> <span data-ttu-id="0f8a7-118">Wenn `PossiblyEatMessage` **true** zurückgibt, wird die Nachricht von **onreceivemess** ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0f8a7-118">If `PossiblyEatMessage` returns **TRUE**, **OnReceiveMessage** ignores the message.</span></span> <span data-ttu-id="0f8a7-119">Eine abgeleitete Klasse kann `PossiblyEatMessage` überschreiben, sodass einige Nachrichten an ein Besitzer Fenster weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="0f8a7-119">A derived class can override `PossiblyEatMessage` so that it forwards some messages to an owner window.</span></span> <span data-ttu-id="0f8a7-120">Beispielsweise leitet die [**cbasecontrolwindow**](cbasecontrolwindow.md) -Klasse, die von **cbasewindow** abgeleitet wird, Tastatur-und Maus Nachrichten weiter.</span><span class="sxs-lookup"><span data-stu-id="0f8a7-120">For example, the [**CBaseControlWindow**](cbasecontrolwindow.md) class, which derives from **CBaseWindow**, forwards keyboard and mouse messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f8a7-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f8a7-121">Requirements</span></span>



| <span data-ttu-id="0f8a7-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f8a7-122">Requirement</span></span> | <span data-ttu-id="0f8a7-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0f8a7-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f8a7-124">Header</span><span class="sxs-lookup"><span data-stu-id="0f8a7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0f8a7-125"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f8a7-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0f8a7-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0f8a7-126">Library</span></span><br/> | <dl> <span data-ttu-id="0f8a7-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0f8a7-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f8a7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f8a7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f8a7-129">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0f8a7-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




