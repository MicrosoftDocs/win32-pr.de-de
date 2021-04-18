---
description: Die setdrawcontext-Methode legt die zum Zeichnen verwendeten Geräte Kontexte fest.
ms.assetid: dd752970-99b3-42bb-95a5-8103cab276da
title: Cdrawimage. setdrawcontext-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetDrawContext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d329dd45d1a02afd2cbd0daf8d0da8390b0b395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358029"
---
# <a name="cdrawimagesetdrawcontext-method"></a><span data-ttu-id="270c2-103">Cdrawimage. setdrawcontext-Methode</span><span class="sxs-lookup"><span data-stu-id="270c2-103">CDrawImage.SetDrawContext method</span></span>

<span data-ttu-id="270c2-104">Die- `SetDrawContext` Methode legt die zum Zeichnen verwendeten Geräte Kontexte fest.</span><span class="sxs-lookup"><span data-stu-id="270c2-104">The `SetDrawContext` method sets the device contexts used for drawing.</span></span>

## <a name="syntax"></a><span data-ttu-id="270c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="270c2-105">Syntax</span></span>


```C++
void SetDrawContext();
```



## <a name="parameters"></a><span data-ttu-id="270c2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="270c2-106">Parameters</span></span>

<span data-ttu-id="270c2-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="270c2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="270c2-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="270c2-108">Return value</span></span>

<span data-ttu-id="270c2-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="270c2-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="270c2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="270c2-110">Remarks</span></span>

<span data-ttu-id="270c2-111">Diese Methode ruft die Fenster-und Arbeitsspeicher-Geräte Kontexte aus dem besitzenden [**cbasewindow**](cbasewindow.md) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="270c2-111">This method retrieves the window and memory device contexts from the owning [**CBaseWindow**](cbasewindow.md) object.</span></span> <span data-ttu-id="270c2-112">Ruft diese Methode auf, nachdem das Fenster initialisiert wurde, jedoch bevor Sie mit dem Zeichnen beginnen.</span><span class="sxs-lookup"><span data-stu-id="270c2-112">Call this method after the window is initialized, but before you begin drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="270c2-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="270c2-113">Requirements</span></span>



| <span data-ttu-id="270c2-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="270c2-114">Requirement</span></span> | <span data-ttu-id="270c2-115">Wert</span><span class="sxs-lookup"><span data-stu-id="270c2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="270c2-116">Header</span><span class="sxs-lookup"><span data-stu-id="270c2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="270c2-117"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="270c2-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="270c2-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="270c2-118">Library</span></span><br/> | <dl> <span data-ttu-id="270c2-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="270c2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="270c2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="270c2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="270c2-121">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="270c2-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




