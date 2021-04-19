---
description: Die get \_ messagedrain-Methode ruft die aktuelle Nachrichten Ableitung ab.
ms.assetid: d679e7f7-4628-479b-b722-843cdd91ffe6
title: CBaseControlWindow.get_MessageDrain-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aaf51c3f4297f238e51bbe8677303730c04b89d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369601"
---
# <a name="cbasecontrolwindowget_messagedrain-method"></a><span data-ttu-id="5342f-103">Cbasecontrolwindow. get \_ messagedrain-Methode</span><span class="sxs-lookup"><span data-stu-id="5342f-103">CBaseControlWindow.get\_MessageDrain method</span></span>

<span data-ttu-id="5342f-104">Die- `get_MessageDrain` Methode ruft den aktuellen Nachrichten Ausgleich ab.</span><span class="sxs-lookup"><span data-stu-id="5342f-104">The `get_MessageDrain` method retrieves the current message drain.</span></span>

## <a name="syntax"></a><span data-ttu-id="5342f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5342f-105">Syntax</span></span>


```C++
HRESULT get_MessageDrain(
   OAHWND *Drain
);
```



## <a name="parameters"></a><span data-ttu-id="5342f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5342f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5342f-107">*Entladen*</span><span class="sxs-lookup"><span data-stu-id="5342f-107">*Drain*</span></span> 
</dt> <dd>

<span data-ttu-id="5342f-108">Zeiger auf das aktuelle Fenster, das Fenster Meldungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="5342f-108">Pointer to the current window receiving window messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5342f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5342f-109">Return value</span></span>

<span data-ttu-id="5342f-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5342f-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5342f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5342f-111">Remarks</span></span>

<span data-ttu-id="5342f-112">Nachrichten, die an den Videorenderer-Filter gesendet werden, können in einem anderen Fenster gepostet werden.</span><span class="sxs-lookup"><span data-stu-id="5342f-112">Messages sent to the video renderer filter can be posted to another window.</span></span> <span data-ttu-id="5342f-113">Das Fenster, das für den Empfang dieser Meldungen registriert ist (mithilfe der **cbasecontrolwindow:: get \_ messagedrain** -Member-Funktion), ist der aktuelle Nachrichten Ausgleich.</span><span class="sxs-lookup"><span data-stu-id="5342f-113">The window registered to receive these messages (using the **CBaseControlWindow::get\_MessageDrain** member function) is the current message drain.</span></span>

## <a name="requirements"></a><span data-ttu-id="5342f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5342f-114">Requirements</span></span>



| <span data-ttu-id="5342f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5342f-115">Requirement</span></span> | <span data-ttu-id="5342f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5342f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5342f-117">Header</span><span class="sxs-lookup"><span data-stu-id="5342f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5342f-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5342f-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5342f-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5342f-119">Library</span></span><br/> | <dl> <span data-ttu-id="5342f-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5342f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5342f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5342f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5342f-122">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5342f-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




