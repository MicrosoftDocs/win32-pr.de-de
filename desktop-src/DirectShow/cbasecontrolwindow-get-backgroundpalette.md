---
description: Die get \_ backgroundpalette-Methode ruft die realisierte Palette im hintergrundflag ab.
ms.assetid: cc649dbd-d049-4993-b187-4e297bef5152
title: CBaseControlWindow.get_BackgroundPalette-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd06bcec9b3c435370ec3f12340c1c3aede3904c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369971"
---
# <a name="cbasecontrolwindowget_backgroundpalette-method"></a><span data-ttu-id="e9b3f-103">Cbasecontrolwindow. get \_ backgroundpalette-Methode</span><span class="sxs-lookup"><span data-stu-id="e9b3f-103">CBaseControlWindow.get\_BackgroundPalette method</span></span>

<span data-ttu-id="e9b3f-104">Die- `get_BackgroundPalette` Methode ruft die realisierte Palette im hintergrundflag ab.</span><span class="sxs-lookup"><span data-stu-id="e9b3f-104">The `get_BackgroundPalette` method retrieves the realized palette in the background flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9b3f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9b3f-105">Syntax</span></span>


```C++
HRESULT get_BackgroundPalette(
   long *pBackgroundPalette
);
```



## <a name="parameters"></a><span data-ttu-id="e9b3f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9b3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9b3f-107">*pbackgroundpalette*</span><span class="sxs-lookup"><span data-stu-id="e9b3f-107">*pBackgroundPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="e9b3f-108">Zeiger auf ein boolesches Automatisierungs Flag (0 ist off, 1 ist on).</span><span class="sxs-lookup"><span data-stu-id="e9b3f-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9b3f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9b3f-109">Return value</span></span>

<span data-ttu-id="e9b3f-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e9b3f-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9b3f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9b3f-111">Remarks</span></span>

<span data-ttu-id="e9b3f-112">Diese Member-Funktion implementiert die Methode [**IVideoWindow:: get \_ backgroundpalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) .</span><span class="sxs-lookup"><span data-stu-id="e9b3f-112">This member function implements the [**IVideoWindow::get\_BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) method.</span></span> <span data-ttu-id="e9b3f-113">Wenn ein Video in einer anderen Anwendung oder einem anderen Dokument abgespielt wird, möchte die Anwendung möglicherweise eine eigene Palette verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9b3f-113">If a video will be played within another application or document, the application might want to use its own palette.</span></span> <span data-ttu-id="e9b3f-114">Es kann gefragt werden, ob das Video die aktuelle Vordergrund Palette anstelle eines eigenen verwendet, indem dieses Flag auf 1 festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e9b3f-114">It can ask that the video use the current foreground palette rather than its own by setting this flag to  1.</span></span> <span data-ttu-id="e9b3f-115">Wenn dieser Wert auf 0 festgelegt ist, wird im Fenster eine eigene bevorzugte Palette installiert und erkannt.</span><span class="sxs-lookup"><span data-stu-id="e9b3f-115">If this is set to 0, the window will install and realize its own preferred palette.</span></span> <span data-ttu-id="e9b3f-116">Beachten Sie, dass die Frage, ob das Fenster eine andere Palette verwendet, zu schwerwiegenden Leistungseinbußen führt.</span><span class="sxs-lookup"><span data-stu-id="e9b3f-116">Note that asking the window to use a different palette will cause severe performance penalties.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9b3f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9b3f-117">Requirements</span></span>



| <span data-ttu-id="e9b3f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9b3f-118">Requirement</span></span> | <span data-ttu-id="e9b3f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e9b3f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9b3f-120">Header</span><span class="sxs-lookup"><span data-stu-id="e9b3f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e9b3f-121"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9b3f-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e9b3f-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e9b3f-122">Library</span></span><br/> | <dl> <span data-ttu-id="e9b3f-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e9b3f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9b3f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9b3f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9b3f-125">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e9b3f-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




