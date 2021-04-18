---
description: Die getwindowposition-Methode ruft die aktuellen Koordinaten für das Fenster ab.
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: Cbasecontrolwindow. getwindowposition-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: af2b1bdb8b2c839644e8c0629e3e272c123d3c21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357678"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a><span data-ttu-id="81e24-103">Cbasecontrolwindow. getwindowposition-Methode</span><span class="sxs-lookup"><span data-stu-id="81e24-103">CBaseControlWindow.GetWindowPosition method</span></span>

<span data-ttu-id="81e24-104">Die- `GetWindowPosition` Methode ruft die aktuellen Koordinaten für das Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="81e24-104">The `GetWindowPosition` method retrieves the current coordinates for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="81e24-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="81e24-105">Syntax</span></span>


```C++
HRESULT GetWindowPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="81e24-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="81e24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81e24-107">*pleft*</span><span class="sxs-lookup"><span data-stu-id="81e24-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="81e24-108">Zeiger auf die linke Koordinate in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="81e24-108">Pointer to the left coordinate, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="81e24-109">*ptop*</span><span class="sxs-lookup"><span data-stu-id="81e24-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="81e24-110">Zeiger auf die obere Koordinate in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="81e24-110">Pointer to the top coordinate, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="81e24-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="81e24-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="81e24-112">Zeiger auf die Fensterbreite in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="81e24-112">Pointer to the window width, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="81e24-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="81e24-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="81e24-114">Zeiger auf die Fensterhöhe in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="81e24-114">Pointer to the window height, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81e24-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81e24-115">Return value</span></span>

<span data-ttu-id="81e24-116">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="81e24-116">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="81e24-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81e24-117">Requirements</span></span>



| <span data-ttu-id="81e24-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81e24-118">Requirement</span></span> | <span data-ttu-id="81e24-119">Wert</span><span class="sxs-lookup"><span data-stu-id="81e24-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81e24-120">Header</span><span class="sxs-lookup"><span data-stu-id="81e24-120">Header</span></span><br/>  | <dl> <span data-ttu-id="81e24-121"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81e24-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="81e24-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="81e24-122">Library</span></span><br/> | <dl> <span data-ttu-id="81e24-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="81e24-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81e24-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81e24-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81e24-125">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="81e24-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




