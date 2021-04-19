---
title: D2D1_COLOR_F (D2DBaseTypes. h)
description: Beschreibt die Komponenten rot, grün, blau und Alpha einer Farbe. | D2D1_COLOR_F (D2DBaseTypes. h)
ms.assetid: 564d4f41-2da7-49ed-b85a-d1070d662b40
keywords:
- D2D1_COLOR_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f12c4c833d7f73946b2309673dff8f3dd11395
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361806"
---
# <a name="d2d1_color_f"></a><span data-ttu-id="e670a-105">D2D1- \_ Farbe \_ F</span><span class="sxs-lookup"><span data-stu-id="e670a-105">D2D1\_COLOR\_F</span></span>

<span data-ttu-id="e670a-106">Beschreibt die Komponenten rot, grün, blau und Alpha einer Farbe.</span><span class="sxs-lookup"><span data-stu-id="e670a-106">Describes the red, green, blue, and alpha components of a color.</span></span>


```C++
typedef D2D_COLOR_F D2D1_COLOR_F;
```



## <a name="remarks"></a><span data-ttu-id="e670a-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e670a-107">Remarks</span></span>

<span data-ttu-id="e670a-108">**D2D1 \_ Color \_ f** ist eine typedef für [**D2D \_ Color \_ f**](d2d-color-f.md), bei der es sich um eine typedef für [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)handelt.</span><span class="sxs-lookup"><span data-stu-id="e670a-108">**D2D1\_COLOR\_F** is a typedef for [**D2D\_COLOR\_F**](d2d-color-f.md), which is itself a typedef for [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span></span> <span data-ttu-id="e670a-109">Informationen zu den von **D2D1 \_ Color \_ F** bereitgestellten Membern finden Sie unter [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="e670a-109">For information about the members provided by **D2D1\_COLOR\_F**, see [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span></span>

<span data-ttu-id="e670a-110">Die [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) -Klasse stellt einen Satz vordefinierter Farben und Hilfsfunktionen zum Definieren von Farben bereit.</span><span class="sxs-lookup"><span data-stu-id="e670a-110">The [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class provides a set of predefined colors and helper functions for defining colors.</span></span> <span data-ttu-id="e670a-111">Weitere Informationen finden Sie in der [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) -Referenz.</span><span class="sxs-lookup"><span data-stu-id="e670a-111">For more information, see the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) reference.</span></span>

## <a name="examples"></a><span data-ttu-id="e670a-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e670a-112">Examples</span></span>

<span data-ttu-id="e670a-113">Im folgenden Beispiel wird die [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) -Klasse verwendet, um beim Erstellen eines [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)eine vordefinierte Farbe (schwarz) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e670a-113">The following example uses the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to specify a predefined color (black) when creating an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```



<span data-ttu-id="e670a-114">Im folgenden Beispiel wird die [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) -Klasse verwendet, um eine Farbe mithilfe von rot-, grün-, blau-und Alpha Werten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e670a-114">The following example uses the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to specify a color using red, green, blue, and alpha values.</span></span>


```C++
ID2D1SolidColorBrush *pGridBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
    &pGridBrush
    );
```



## <a name="requirements"></a><span data-ttu-id="e670a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e670a-115">Requirements</span></span>



| <span data-ttu-id="e670a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e670a-116">Requirement</span></span> | <span data-ttu-id="e670a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e670a-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e670a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e670a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e670a-119">Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e670a-119">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="e670a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e670a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e670a-121">Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e670a-121">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="e670a-122">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="e670a-122">Minimum supported phone</span></span><br/>  | <span data-ttu-id="e670a-123">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="e670a-123">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="e670a-124">Header</span><span class="sxs-lookup"><span data-stu-id="e670a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e670a-125"><dt>D2DBaseTypes. h (Include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e670a-125"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e670a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e670a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e670a-127">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="e670a-127">D3DCOLORVALUE</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="e670a-128">**Colorf**</span><span class="sxs-lookup"><span data-stu-id="e670a-128">**ColorF**</span></span>](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)
</dt> </dl>

 

