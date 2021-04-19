---
description: Die Put \_ Owner-Methode legt das übergeordnete Fenster des Videofensters fest. das übergeordnete Fenster leitet dann bestimmte Meldungen an das Videofenster weiter.
ms.assetid: 8ed85cb0-47be-40c1-947a-dd9f7850d867
title: CBaseControlWindow.put_Owner-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16817d1c3f0fbdf756f6c054b875b8507fd1172a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359752"
---
# <a name="cbasecontrolwindowput_owner-method"></a><span data-ttu-id="7f460-103">Cbasecontrolwindow. Put \_ Owner-Methode</span><span class="sxs-lookup"><span data-stu-id="7f460-103">CBaseControlWindow.put\_Owner method</span></span>

<span data-ttu-id="7f460-104">Die `put_Owner` -Methode legt das übergeordnete Fenster des Videofensters fest. das übergeordnete Fenster leitet dann bestimmte Meldungen an das Videofenster weiter.</span><span class="sxs-lookup"><span data-stu-id="7f460-104">The `put_Owner` method sets the video window's parent window; the parent window then forwards certain messages to the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f460-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f460-105">Syntax</span></span>


```C++
HRESULT put_Owner(
   OAHWND Owner
);
```



## <a name="parameters"></a><span data-ttu-id="7f460-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f460-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f460-107">*Besitzer*</span><span class="sxs-lookup"><span data-stu-id="7f460-107">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="7f460-108">Handle für das übergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="7f460-108">Handle to the parent window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f460-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f460-109">Return value</span></span>

<span data-ttu-id="7f460-110">Gibt noError zurück.</span><span class="sxs-lookup"><span data-stu-id="7f460-110">Returns NOERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f460-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f460-111">Remarks</span></span>

<span data-ttu-id="7f460-112">Intern ruft diese Methode die Microsoft Win32 **SetParent** -Funktion auf, um den neuen Besitzer festzulegen, und legt den Stil des übergeordneten Fensters auf WS \_ Child fest.</span><span class="sxs-lookup"><span data-stu-id="7f460-112">Internally, this method calls the Microsoft Win32 **SetParent** function to set the new owner and sets the parent window's style to WS\_CHILD.</span></span> <span data-ttu-id="7f460-113">Das übergeordnete Fenster führt dann bestimmte Nachrichten Sätze (insbesondere Maus-und Tastatur Meldungen) an das Videofenster weiter.</span><span class="sxs-lookup"><span data-stu-id="7f460-113">The parent window will then forward certain sets of messages (in particular, mouse and keyboard messages) to the video window.</span></span>

<span data-ttu-id="7f460-114">Nachdem Sie den Besitzer des Videofensters festgelegt haben, müssen Sie für den Besitzer den Wert **null** festlegen, und der Fenster Stil des Besitzers muss auf WS überlappende \_ und WS clipchildren festgelegt werden, \_ bevor das Filter Diagramm freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7f460-114">After you set the video window's owner, you must set the owner to **NULL** and the owner's window style to WS\_OVERLAPPED and WS\_CLIPCHILDREN before releasing the filter graph.</span></span> <span data-ttu-id="7f460-115">Wenn Sie den Besitzer auf **null** festlegen, deaktiviert diese Methode das untergeordnete WS-Bit des übergeordneten Fensters \_ .</span><span class="sxs-lookup"><span data-stu-id="7f460-115">When you set the owner to **NULL**, this method turns off the parent window's WS\_CHILD bit.</span></span> <span data-ttu-id="7f460-116">Wenn Sie den Besitzer nicht auf **null** festlegen, übergibt das übergeordnete Fenster weiterhin Meldungen an das Videofenster, und es treten wahrscheinlich Fehler auf, wenn die Anwendung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="7f460-116">If you don't set the owner to **NULL**, the parent window will continue to pass messages to the video window and errors will likely occur when the application closes.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f460-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f460-117">Requirements</span></span>



| <span data-ttu-id="7f460-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f460-118">Requirement</span></span> | <span data-ttu-id="7f460-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7f460-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f460-120">Header</span><span class="sxs-lookup"><span data-stu-id="7f460-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7f460-121"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f460-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7f460-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7f460-122">Library</span></span><br/> | <dl> <span data-ttu-id="7f460-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7f460-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f460-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f460-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f460-125">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7f460-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




