---
description: Mit der Put- \_ Methode WindowStyle werden die Standardfenster Stile festgelegt.
ms.assetid: 3b3aa035-6aa1-4f11-80d8-03268fcf98e1
title: CBaseControlWindow.put_WindowStyle-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f98e6205a45530a0dbcce09d095dfaa2267ccbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361060"
---
# <a name="cbasecontrolwindowput_windowstyle-method"></a><span data-ttu-id="f5601-103">Cbasecontrolwindow. Put \_ WindowStyle-Methode</span><span class="sxs-lookup"><span data-stu-id="f5601-103">CBaseControlWindow.put\_WindowStyle method</span></span>

<span data-ttu-id="f5601-104">Die- `put_WindowStyle` Methode legt die Standardfenster Stile fest.</span><span class="sxs-lookup"><span data-stu-id="f5601-104">The `put_WindowStyle` method sets the standard window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5601-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5601-105">Syntax</span></span>


```C++
HRESULT put_WindowStyle(
   long WindowStyle
);
```



## <a name="parameters"></a><span data-ttu-id="f5601-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5601-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5601-107">*WindowStyle*</span><span class="sxs-lookup"><span data-stu-id="f5601-107">*WindowStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="f5601-108">Neue Fenster Stile.</span><span class="sxs-lookup"><span data-stu-id="f5601-108">New window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5601-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5601-109">Return value</span></span>

<span data-ttu-id="f5601-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f5601-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f5601-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f5601-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5601-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5601-112">Remarks</span></span>

<span data-ttu-id="f5601-113">Achten Sie darauf, die Fenster Stile zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f5601-113">Take care when changing the window styles.</span></span> <span data-ttu-id="f5601-114">In den meisten Fällen sollte eine Anwendung den aktuellen Stil abrufen und dann die unpassenden Bits hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="f5601-114">In most cases, an application should retrieve the current style and then add or remove the inappropriate bits.</span></span> <span data-ttu-id="f5601-115">Diese Prozedur ermöglicht es, dass verschiedene interne Fenster Stile, die von Windows verwendet werden, intakt bleiben.</span><span class="sxs-lookup"><span data-stu-id="f5601-115">This procedure allows various internal window styles used by Windows to remain intact.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5601-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5601-116">Requirements</span></span>



| <span data-ttu-id="f5601-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5601-117">Requirement</span></span> | <span data-ttu-id="f5601-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f5601-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5601-119">Header</span><span class="sxs-lookup"><span data-stu-id="f5601-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f5601-120"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5601-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f5601-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f5601-121">Library</span></span><br/> | <dl> <span data-ttu-id="f5601-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f5601-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5601-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5601-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5601-124">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f5601-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




