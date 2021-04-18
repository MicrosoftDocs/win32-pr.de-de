---
description: Die Put \_ backgroundpalette-Methode legt ein Flag fest, um die Palette im Hintergrund zu erkennen.
ms.assetid: db420e75-e300-41fa-bae4-fb267cc99c7c
title: CBaseControlWindow.put_BackgroundPalette-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04aeb445be91426e7995ecd01c9326cda586a447
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371125"
---
# <a name="cbasecontrolwindowput_backgroundpalette-method"></a><span data-ttu-id="9c19a-103">Cbasecontrolwindow. Put \_ backgroundpalette-Methode</span><span class="sxs-lookup"><span data-stu-id="9c19a-103">CBaseControlWindow.put\_BackgroundPalette method</span></span>

<span data-ttu-id="9c19a-104">Die- `put_BackgroundPalette` Methode legt ein Flag fest, um die Palette im Hintergrund zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="9c19a-104">The `put_BackgroundPalette` method sets a flag to realize the palette in the background.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c19a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c19a-105">Syntax</span></span>


```C++
HRESULT put_BackgroundPalette(
   long BackgroundPalette
);
```



## <a name="parameters"></a><span data-ttu-id="9c19a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c19a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c19a-107">*Backgroundpalette*</span><span class="sxs-lookup"><span data-stu-id="9c19a-107">*BackgroundPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="9c19a-108">Boolesches Automatisierungs Flag (0 ist off, 1 ist on).</span><span class="sxs-lookup"><span data-stu-id="9c19a-108">Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c19a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c19a-109">Return value</span></span>

<span data-ttu-id="9c19a-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9c19a-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c19a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c19a-111">Remarks</span></span>

<span data-ttu-id="9c19a-112">Zum Abspielen eines Videos in einer anderen Anwendung oder einem anderen Dokument möchte die Anwendung möglicherweise eine eigene Palette verwenden.</span><span class="sxs-lookup"><span data-stu-id="9c19a-112">To play a video within another application or document, the application might want to use its own palette.</span></span> <span data-ttu-id="9c19a-113">Das Video kann die aktuelle Vordergrund Palette anstelle seiner eigenen als Hintergrund Palette verwenden, indem dieses Flag auf 1 festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="9c19a-113">It can ask that the video use the current foreground palette rather than its own as the background palette by setting this flag to  1.</span></span> <span data-ttu-id="9c19a-114">Wenn dieser Wert auf 0 festgelegt ist, wird im Fenster eine eigene bevorzugte Palette installiert und erkannt.</span><span class="sxs-lookup"><span data-stu-id="9c19a-114">If this is set to 0, the window will install and realize its own preferred palette.</span></span> <span data-ttu-id="9c19a-115">Wenn Sie das Fenster zur Verwendung einer anderen Palette auffordern, werden schwerwiegende Leistungseinbußen verursacht.</span><span class="sxs-lookup"><span data-stu-id="9c19a-115">Asking the window to use a different palette will cause severe performance penalties.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c19a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c19a-116">Requirements</span></span>



| <span data-ttu-id="9c19a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c19a-117">Requirement</span></span> | <span data-ttu-id="9c19a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9c19a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c19a-119">Header</span><span class="sxs-lookup"><span data-stu-id="9c19a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9c19a-120"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c19a-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9c19a-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9c19a-121">Library</span></span><br/> | <dl> <span data-ttu-id="9c19a-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9c19a-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c19a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c19a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c19a-124">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9c19a-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




