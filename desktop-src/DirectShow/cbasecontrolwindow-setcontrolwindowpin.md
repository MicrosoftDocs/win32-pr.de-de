---
description: Die setcontrolwindowpin-Methode legt die PIN fest, mit der synchronisiert werden soll.
ms.assetid: 6373c046-5448-4159-88b9-9b2babdb938b
title: Cbasecontrolwindow. setcontrolwindowpin-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetControlWindowPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1aa3d4960799c2286e17709258ea90b76332bc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362155"
---
# <a name="cbasecontrolwindowsetcontrolwindowpin-method"></a><span data-ttu-id="a143b-103">Cbasecontrolwindow. setcontrolwindowpin-Methode</span><span class="sxs-lookup"><span data-stu-id="a143b-103">CBaseControlWindow.SetControlWindowPin method</span></span>

<span data-ttu-id="a143b-104">Die- `SetControlWindowPin` Methode legt die PIN fest, mit der synchronisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a143b-104">The `SetControlWindowPin` method sets the pin with which to synchronize.</span></span>

## <a name="syntax"></a><span data-ttu-id="a143b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a143b-105">Syntax</span></span>


```C++
void SetControlWindowPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="a143b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a143b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a143b-107">*ppin*</span><span class="sxs-lookup"><span data-stu-id="a143b-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="a143b-108">Zeiger auf die PIN, mit der die Schnittstelle synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a143b-108">Pointer to the pin with which the interface is synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a143b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a143b-109">Return value</span></span>

<span data-ttu-id="a143b-110">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="a143b-110">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a143b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a143b-111">Remarks</span></span>

<span data-ttu-id="a143b-112">Diese Member-Funktion legt die m \_ ppin-Member-Variable auf den ppin-Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="a143b-112">This member function sets the m\_pPin member variable equal to the pPin parameter.</span></span> <span data-ttu-id="a143b-113">Wie im-Konstruktor beschrieben, kann die-Schnittstelle nur aufgerufen werden, wenn der Filter erfolgreich verbunden wurde.</span><span class="sxs-lookup"><span data-stu-id="a143b-113">As described in the constructor, the interface can be called only when the filter has been connected successfully.</span></span> <span data-ttu-id="a143b-114">Das Objekt wird über diese Element Funktion an die PIN übergeben, mit der es synchronisiert werden soll. in den meisten Fällen wird festgestellt, ob die PIN verbunden ist, wenn Sie über eine Schnittstellen Methode mit dem Namen verfügt, und \_ \_ \_ Wenn Sie fehlschlägt, wird VFW E nicht verbunden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a143b-114">The object is passed in through this member function to the pin with which it should synchronize; in most cases, it will determine if the pin is connected whenever it has an interface method called and will return VFW\_E\_NOT\_CONNECTED if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="a143b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a143b-115">Requirements</span></span>



| <span data-ttu-id="a143b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a143b-116">Requirement</span></span> | <span data-ttu-id="a143b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a143b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a143b-118">Header</span><span class="sxs-lookup"><span data-stu-id="a143b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a143b-119"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a143b-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a143b-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a143b-120">Library</span></span><br/> | <dl> <span data-ttu-id="a143b-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a143b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a143b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a143b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a143b-123">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a143b-123">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




