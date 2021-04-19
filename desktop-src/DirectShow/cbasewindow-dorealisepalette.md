---
description: Die Methode "dorealilpalette" erkennt die aktuelle Palette des Fensters.
ms.assetid: dd023c81-0cd0-48c6-bc63-5891f2a4acf7
title: Cbasewindow. dorealilpalette-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoRealisePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be1e02d355ab5991c9d0e95dbff30d4c8e0162ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368309"
---
# <a name="cbasewindowdorealisepalette-method"></a><span data-ttu-id="98e78-103">Cbasewindow. dorealilpalette-Methode</span><span class="sxs-lookup"><span data-stu-id="98e78-103">CBaseWindow.DoRealisePalette method</span></span>

<span data-ttu-id="98e78-104">Die `DoRealisePalette` -Methode erkennt die aktuelle Palette des Fensters.</span><span class="sxs-lookup"><span data-stu-id="98e78-104">The `DoRealisePalette` method realizes the window's current palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e78-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="98e78-105">Syntax</span></span>


```C++
virtual HRESULT DoRealisePalette(
   BOOL bForceBackground
);
```



## <a name="parameters"></a><span data-ttu-id="98e78-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="98e78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98e78-107">*bForceBackground*</span><span class="sxs-lookup"><span data-stu-id="98e78-107">*bForceBackground*</span></span> 
</dt> <dd>

<span data-ttu-id="98e78-108">Boolescher Wert, der angibt, ob die Palette als Hintergrund Palette erzwungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="98e78-108">Boolean value that specifies whether the palette is forced to be a background palette.</span></span> <span data-ttu-id="98e78-109">Weitere Informationen finden Sie unter **SelectPalette** im Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="98e78-109">For more information, see **SelectPalette** in the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98e78-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98e78-110">Return value</span></span>

<span data-ttu-id="98e78-111">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="98e78-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="98e78-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="98e78-112">Return code</span></span>                                                                             | <span data-ttu-id="98e78-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98e78-113">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="98e78-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="98e78-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="98e78-115">Ein interner-Befehl von " **gdiflush** " hat einen Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="98e78-115">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="98e78-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="98e78-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="98e78-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="98e78-117">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="98e78-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98e78-118">Remarks</span></span>

<span data-ttu-id="98e78-119">Die [**cbasewindow:: onpalettechange**](cbasewindow-onpalettechange.md) -Methode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="98e78-119">The [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method calls this method.</span></span> <span data-ttu-id="98e78-120">Um eine neue Palette festzulegen, müssen Sie die [**cbasewindow:: SetPalette**](cbasewindow-setpalette.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="98e78-120">To set a new palette, call the [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="98e78-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98e78-121">Requirements</span></span>



| <span data-ttu-id="98e78-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98e78-122">Requirement</span></span> | <span data-ttu-id="98e78-123">Wert</span><span class="sxs-lookup"><span data-stu-id="98e78-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98e78-124">Header</span><span class="sxs-lookup"><span data-stu-id="98e78-124">Header</span></span><br/>  | <dl> <span data-ttu-id="98e78-125"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98e78-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="98e78-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="98e78-126">Library</span></span><br/> | <dl> <span data-ttu-id="98e78-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="98e78-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e78-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98e78-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e78-129">**Cbasewindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="98e78-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




