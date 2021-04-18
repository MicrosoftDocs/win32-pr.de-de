---
description: Die Methode "possiblyeatmessage" leitet Tastatur-und Maus Meldungen an das Fenster "Nachrichten Ausgleich" weiter.
ms.assetid: 8e344c5d-2f94-454f-89b7-45c539b6e833
title: Cbasecontrolwindow. possiblyeatmessage-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bfadcfbbd6833d8f3e9b65bd39d0cdbef4a006e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351291"
---
# <a name="cbasecontrolwindowpossiblyeatmessage-method"></a><span data-ttu-id="ec75a-103">Cbasecontrolwindow. possiblyeatmessage-Methode</span><span class="sxs-lookup"><span data-stu-id="ec75a-103">CBaseControlWindow.PossiblyEatMessage method</span></span>

<span data-ttu-id="ec75a-104">Die `PossiblyEatMessage` -Methode leitet Tastatur-und Maus Meldungen an das Fenster für die Nachrichten Ableitung weiter.</span><span class="sxs-lookup"><span data-stu-id="ec75a-104">The `PossiblyEatMessage` method forwards keyboard and mouse messages to the message-drain window.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec75a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec75a-105">Syntax</span></span>


```C++
BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="ec75a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec75a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec75a-107">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="ec75a-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="ec75a-108">Fenster Meldung.</span><span class="sxs-lookup"><span data-stu-id="ec75a-108">Window message.</span></span>

</dd> <dt>

<span data-ttu-id="ec75a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec75a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec75a-110">Der erste Message-Parameter.</span><span class="sxs-lookup"><span data-stu-id="ec75a-110">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ec75a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec75a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec75a-112">Der zweite Meldungs Parameter.</span><span class="sxs-lookup"><span data-stu-id="ec75a-112">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec75a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec75a-113">Return value</span></span>

<span data-ttu-id="ec75a-114">Gibt **true** zurück, wenn die Nachricht an das Fenster weitergeleitet wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="ec75a-114">Returns **TRUE** if the message was forwarded to the window, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec75a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec75a-115">Remarks</span></span>

<span data-ttu-id="ec75a-116">Das Fenster für die Nachrichten Ableitung ist ein Fenster, das für den Empfang bestimmter Maus-und Tastatur Meldungen vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="ec75a-116">The message-drain window is a window designated to receive certain mouse and keyboard messages.</span></span> <span data-ttu-id="ec75a-117">Anfänglich ist das Fenster **null**. Sie kann durch Aufrufen von [**cbasecontrolwindow::p UT \_ messagedrain**](cbasecontrolwindow-put-messagedrain.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ec75a-117">Initially the window is **NULL**; it can be set by calling [**CBaseControlWindow::put\_MessageDrain**](cbasecontrolwindow-put-messagedrain.md).</span></span>

<span data-ttu-id="ec75a-118">Wenn das Fenster für die Nachrichten Ableitung nicht **null** ist, werden `PossiblyEatMessage` die folgenden Meldungen an dieses Fenster gesendet:</span><span class="sxs-lookup"><span data-stu-id="ec75a-118">If the message-drain window is non-**NULL**, `PossiblyEatMessage` posts the following messages to that window:</span></span>

-   <span data-ttu-id="ec75a-119">WM \_ -Zeichen</span><span class="sxs-lookup"><span data-stu-id="ec75a-119">WM\_CHAR</span></span>
-   <span data-ttu-id="ec75a-120">WM \_ deadchar</span><span class="sxs-lookup"><span data-stu-id="ec75a-120">WM\_DEADCHAR</span></span>
-   <span data-ttu-id="ec75a-121">WM- \_ KeyDown</span><span class="sxs-lookup"><span data-stu-id="ec75a-121">WM\_KEYDOWN</span></span>
-   <span data-ttu-id="ec75a-122">WM- \_ KeyUp</span><span class="sxs-lookup"><span data-stu-id="ec75a-122">WM\_KEYUP</span></span>
-   <span data-ttu-id="ec75a-123">WM \_ lbuttondblclk</span><span class="sxs-lookup"><span data-stu-id="ec75a-123">WM\_LBUTTONDBLCLK</span></span>
-   <span data-ttu-id="ec75a-124">WM \_ lbuttondown</span><span class="sxs-lookup"><span data-stu-id="ec75a-124">WM\_LBUTTONDOWN</span></span>
-   <span data-ttu-id="ec75a-125">WM- \_ lbuttonup</span><span class="sxs-lookup"><span data-stu-id="ec75a-125">WM\_LBUTTONUP</span></span>
-   <span data-ttu-id="ec75a-126">WM- \_ mbuttondblclk</span><span class="sxs-lookup"><span data-stu-id="ec75a-126">WM\_MBUTTONDBLCLK</span></span>
-   <span data-ttu-id="ec75a-127">WM- \_ mbuttondown</span><span class="sxs-lookup"><span data-stu-id="ec75a-127">WM\_MBUTTONDOWN</span></span>
-   <span data-ttu-id="ec75a-128">WM- \_ mbuttonup</span><span class="sxs-lookup"><span data-stu-id="ec75a-128">WM\_MBUTTONUP</span></span>
-   <span data-ttu-id="ec75a-129">WM- \_ moueinaktivierung</span><span class="sxs-lookup"><span data-stu-id="ec75a-129">WM\_MOUSEACTIVATE</span></span>
-   <span data-ttu-id="ec75a-130">WM- \_ mouseelmove</span><span class="sxs-lookup"><span data-stu-id="ec75a-130">WM\_MOUSEMOVE</span></span>
-   <span data-ttu-id="ec75a-131">WM \_ nclbuttondblclk</span><span class="sxs-lookup"><span data-stu-id="ec75a-131">WM\_NCLBUTTONDBLCLK</span></span>
-   <span data-ttu-id="ec75a-132">WM- \_ nclbuttondown</span><span class="sxs-lookup"><span data-stu-id="ec75a-132">WM\_NCLBUTTONDOWN</span></span>
-   <span data-ttu-id="ec75a-133">WM- \_ nclbuttonup</span><span class="sxs-lookup"><span data-stu-id="ec75a-133">WM\_NCLBUTTONUP</span></span>
-   <span data-ttu-id="ec75a-134">WM \_ ncmbuttondblclk</span><span class="sxs-lookup"><span data-stu-id="ec75a-134">WM\_NCMBUTTONDBLCLK</span></span>
-   <span data-ttu-id="ec75a-135">WM \_ ncmbuttondown</span><span class="sxs-lookup"><span data-stu-id="ec75a-135">WM\_NCMBUTTONDOWN</span></span>
-   <span data-ttu-id="ec75a-136">WM \_ ncmbuttonup</span><span class="sxs-lookup"><span data-stu-id="ec75a-136">WM\_NCMBUTTONUP</span></span>
-   <span data-ttu-id="ec75a-137">WM- \_ ncmouummove</span><span class="sxs-lookup"><span data-stu-id="ec75a-137">WM\_NCMOUSEMOVE</span></span>
-   <span data-ttu-id="ec75a-138">WM \_ ncrbuttondblclk</span><span class="sxs-lookup"><span data-stu-id="ec75a-138">WM\_NCRBUTTONDBLCLK</span></span>
-   <span data-ttu-id="ec75a-139">WM- \_ ncrbuttondown</span><span class="sxs-lookup"><span data-stu-id="ec75a-139">WM\_NCRBUTTONDOWN</span></span>
-   <span data-ttu-id="ec75a-140">WM- \_ ncrbuttonup</span><span class="sxs-lookup"><span data-stu-id="ec75a-140">WM\_NCRBUTTONUP</span></span>
-   <span data-ttu-id="ec75a-141">WM- \_ rbuttondblclk</span><span class="sxs-lookup"><span data-stu-id="ec75a-141">WM\_RBUTTONDBLCLK</span></span>
-   <span data-ttu-id="ec75a-142">WM- \_ rbuttondown</span><span class="sxs-lookup"><span data-stu-id="ec75a-142">WM\_RBUTTONDOWN</span></span>
-   <span data-ttu-id="ec75a-143">WM- \_ rbuttonup</span><span class="sxs-lookup"><span data-stu-id="ec75a-143">WM\_RBUTTONUP</span></span>
-   <span data-ttu-id="ec75a-144">WM- \_ syschar</span><span class="sxs-lookup"><span data-stu-id="ec75a-144">WM\_SYSCHAR</span></span>
-   <span data-ttu-id="ec75a-145">WM \_ sysdeadchar</span><span class="sxs-lookup"><span data-stu-id="ec75a-145">WM\_SYSDEADCHAR</span></span>
-   <span data-ttu-id="ec75a-146">WM \_ syskeydown</span><span class="sxs-lookup"><span data-stu-id="ec75a-146">WM\_SYSKEYDOWN</span></span>
-   <span data-ttu-id="ec75a-147">WM- \_ syskeyup</span><span class="sxs-lookup"><span data-stu-id="ec75a-147">WM\_SYSKEYUP</span></span>

<span data-ttu-id="ec75a-148">Andere Meldungen werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ec75a-148">It ignores other messages.</span></span> <span data-ttu-id="ec75a-149">Wenn das Fenster für die Nachrichten Ableitung **null** ist, ignoriert die Methode alle Fenster Meldungen.</span><span class="sxs-lookup"><span data-stu-id="ec75a-149">If the message-drain window is **NULL**, the method ignores all window messages.</span></span> <span data-ttu-id="ec75a-150">Die Methode gibt " **true** " zurück, wenn Sie die Nachricht sendet, andernfalls " **false** ".</span><span class="sxs-lookup"><span data-stu-id="ec75a-150">The method returns **TRUE** if it posts the message, or **FALSE** otherwise.</span></span> <span data-ttu-id="ec75a-151">Die **cbasewindow** -Klasse ruft diese Methode auf, wenn Sie eine Fenster Meldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="ec75a-151">The **CBaseWindow** class calls this method when it receives a window message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec75a-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec75a-152">Requirements</span></span>



| <span data-ttu-id="ec75a-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec75a-153">Requirement</span></span> | <span data-ttu-id="ec75a-154">Wert</span><span class="sxs-lookup"><span data-stu-id="ec75a-154">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec75a-155">Header</span><span class="sxs-lookup"><span data-stu-id="ec75a-155">Header</span></span><br/>  | <dl> <span data-ttu-id="ec75a-156"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec75a-156"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ec75a-157">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ec75a-157">Library</span></span><br/> | <dl> <span data-ttu-id="ec75a-158">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ec75a-158"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec75a-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec75a-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec75a-160">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ec75a-160">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




