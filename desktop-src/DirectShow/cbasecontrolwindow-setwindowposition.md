---
description: Die SetWindowPosition-Methode legt die Fensterposition auf dem Desktop fest.
ms.assetid: 1c2706dd-d67c-41c7-b672-3c040f37bc41
title: Cbasecontrolwindow. SetWindowPosition-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5e92581db4d04d622f5dba5fbfe1c2c4a53b4ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368619"
---
# <a name="cbasecontrolwindowsetwindowposition-method"></a><span data-ttu-id="33f38-103">Cbasecontrolwindow. SetWindowPosition-Methode</span><span class="sxs-lookup"><span data-stu-id="33f38-103">CBaseControlWindow.SetWindowPosition method</span></span>

<span data-ttu-id="33f38-104">Die `SetWindowPosition` -Methode legt die Fensterposition auf dem Desktop fest.</span><span class="sxs-lookup"><span data-stu-id="33f38-104">The `SetWindowPosition` method sets the window position on the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="33f38-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33f38-105">Syntax</span></span>


```C++
HRESULT SetWindowPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="33f38-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="33f38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33f38-107">*Left*</span><span class="sxs-lookup"><span data-stu-id="33f38-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="33f38-108">Neue linke Koordinate.</span><span class="sxs-lookup"><span data-stu-id="33f38-108">New left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="33f38-109">*Top*</span><span class="sxs-lookup"><span data-stu-id="33f38-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="33f38-110">Neue obere Koordinate.</span><span class="sxs-lookup"><span data-stu-id="33f38-110">New top coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="33f38-111">*Width*</span><span class="sxs-lookup"><span data-stu-id="33f38-111">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="33f38-112">Breite des Fensters.</span><span class="sxs-lookup"><span data-stu-id="33f38-112">Width of the window.</span></span>

</dd> <dt>

<span data-ttu-id="33f38-113">*Height*</span><span class="sxs-lookup"><span data-stu-id="33f38-113">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="33f38-114">Höhe des Fensters.</span><span class="sxs-lookup"><span data-stu-id="33f38-114">Height of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33f38-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33f38-115">Return value</span></span>

<span data-ttu-id="33f38-116">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="33f38-116">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="33f38-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33f38-117">Requirements</span></span>



| <span data-ttu-id="33f38-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33f38-118">Requirement</span></span> | <span data-ttu-id="33f38-119">Wert</span><span class="sxs-lookup"><span data-stu-id="33f38-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33f38-120">Header</span><span class="sxs-lookup"><span data-stu-id="33f38-120">Header</span></span><br/>  | <dl> <span data-ttu-id="33f38-121"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33f38-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="33f38-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="33f38-122">Library</span></span><br/> | <dl> <span data-ttu-id="33f38-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="33f38-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33f38-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33f38-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33f38-125">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="33f38-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




