---
description: Die Put \_ messagedrain-Methode legt das Fenster fest, um Fenster Meldungen zu empfangen, die an den Videorenderer gesendet werden.
ms.assetid: b2d2d489-a66f-474a-b8bf-b019179f6f69
title: CBaseControlWindow.put_MessageDrain-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f03f944a6af6ac99de6000a2507178eea510c06a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354751"
---
# <a name="cbasecontrolwindowput_messagedrain-method"></a><span data-ttu-id="225ea-103">Cbasecontrolwindow. Put \_ messagedrain-Methode</span><span class="sxs-lookup"><span data-stu-id="225ea-103">CBaseControlWindow.put\_MessageDrain method</span></span>

<span data-ttu-id="225ea-104">Die- `put_MessageDrain` Methode legt das Fenster fest, um Fenster Meldungen zu empfangen, die an den Videorenderer gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="225ea-104">The `put_MessageDrain` method sets the window to receive window messages sent to the video renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="225ea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="225ea-105">Syntax</span></span>


```C++
HRESULT put_MessageDrain(
   OAHWND Drain
);
```



## <a name="parameters"></a><span data-ttu-id="225ea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="225ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="225ea-107">*Entladen*</span><span class="sxs-lookup"><span data-stu-id="225ea-107">*Drain*</span></span> 
</dt> <dd>

<span data-ttu-id="225ea-108">Fenster, an das Nachrichten gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="225ea-108">Window to post messages to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="225ea-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="225ea-109">Return value</span></span>

<span data-ttu-id="225ea-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="225ea-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="225ea-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="225ea-111">Remarks</span></span>

<span data-ttu-id="225ea-112">Nachrichten, die an den Videorenderer-Filter gesendet werden, können in einem anderen Fenster gepostet werden.</span><span class="sxs-lookup"><span data-stu-id="225ea-112">Messages sent to the video renderer filter can be posted to another window.</span></span> <span data-ttu-id="225ea-113">Diese Member-Funktion registriert das Fenster, um diese Nachrichten zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="225ea-113">This member function registers the window to receive these messages.</span></span> <span data-ttu-id="225ea-114">Anders als bei der [**cbasecontrolwindow::p UT- \_ Besitzer**](cbasecontrolwindow-put-owner.md) Element Funktion macht diese Member-Funktion das Videofenster nicht als untergeordnetes Element eines anderen Fensters.</span><span class="sxs-lookup"><span data-stu-id="225ea-114">Unlike the [**CBaseControlWindow::put\_Owner**](cbasecontrolwindow-put-owner.md) member function, this member function does not make the video window a child of another window.</span></span> <span data-ttu-id="225ea-115">Er ist besonders nützlich für Vollbild-Videorenderer, die keine untergeordneten Fenster sein können.</span><span class="sxs-lookup"><span data-stu-id="225ea-115">It is particularly useful for full-screen video renderers, which cannot be child windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="225ea-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="225ea-116">Requirements</span></span>



| <span data-ttu-id="225ea-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="225ea-117">Requirement</span></span> | <span data-ttu-id="225ea-118">Wert</span><span class="sxs-lookup"><span data-stu-id="225ea-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="225ea-119">Header</span><span class="sxs-lookup"><span data-stu-id="225ea-119">Header</span></span><br/>  | <dl> <span data-ttu-id="225ea-120"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="225ea-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="225ea-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="225ea-121">Library</span></span><br/> | <dl> <span data-ttu-id="225ea-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="225ea-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="225ea-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="225ea-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="225ea-124">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="225ea-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




