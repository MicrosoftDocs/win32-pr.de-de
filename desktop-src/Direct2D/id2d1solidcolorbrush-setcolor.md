---
title: ID2D1SolidColorBrush SetColor-Methoden
description: Gibt die Farbe dieses Pinsel mit voll Tonfarbe an.
ms.assetid: 2900bf72-9641-419c-b0d7-334f14f8a474
keywords:
- SetColor-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 580778135e840a69342ff34ffd8e415883317517
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362047"
---
# <a name="id2d1solidcolorbrushsetcolor-methods"></a><span data-ttu-id="599c5-104">ID2D1SolidColorBrush:: SetColor-Methoden</span><span class="sxs-lookup"><span data-stu-id="599c5-104">ID2D1SolidColorBrush::SetColor methods</span></span>

<span data-ttu-id="599c5-105">Gibt die Farbe dieses Pinsel mit voll Tonfarbe an.</span><span class="sxs-lookup"><span data-stu-id="599c5-105">Specifies the color of this solid color brush.</span></span>

### <a name="overload-list"></a><span data-ttu-id="599c5-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="599c5-106">Overload list</span></span>



| <span data-ttu-id="599c5-107">Methode</span><span class="sxs-lookup"><span data-stu-id="599c5-107">Method</span></span>                                                                          | <span data-ttu-id="599c5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="599c5-108">Description</span></span>                                                |
|:--------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span data-ttu-id="599c5-109">[**SetColor (D2D1 \_ Color \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))</span><span class="sxs-lookup"><span data-stu-id="599c5-109">[**SetColor(D2D1\_COLOR\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))</span></span>  | <span data-ttu-id="599c5-110">Gibt die Farbe dieses Pinsel mit voll Tonfarbe an.</span><span class="sxs-lookup"><span data-stu-id="599c5-110">Specifies the color of this solid-color brush.</span></span> <br/> |
| <span data-ttu-id="599c5-111">[**SetColor (D2D1 \_ Color \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f))</span><span class="sxs-lookup"><span data-stu-id="599c5-111">[**SetColor(D2D1\_COLOR\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f))</span></span> | <span data-ttu-id="599c5-112">Gibt die Farbe dieses Pinsel mit voll Tonfarbe an.</span><span class="sxs-lookup"><span data-stu-id="599c5-112">Specifies the color of this solid color brush.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="599c5-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="599c5-113">Remarks</span></span>

<span data-ttu-id="599c5-114">Zur Unterstützung der Erstellung von Farben bietet Direct2D die [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="599c5-114">To help create colors, Direct2D provides the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class.</span></span> <span data-ttu-id="599c5-115">Es bietet mehrere Hilfsmethoden zum Erstellen von Farben und stellt eine Menge oder vordefinierte Farben bereit.</span><span class="sxs-lookup"><span data-stu-id="599c5-115">It offers several helper methods for creating colors and provides a set or predefined colors.</span></span>

## <a name="examples"></a><span data-ttu-id="599c5-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="599c5-116">Examples</span></span>

<span data-ttu-id="599c5-117">Der folgende Code zeigt, wie diese Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="599c5-117">The following code shows how to use this method.</span></span>


```C++
        m_pSolidColorBrush->SetColor(
            D2D1::ColorF(
                0.0f,
                intensity,
                1.0f - intensity
                ));

        hr = m_pRealization->Fill(
                m_pRT,
                m_pSolidColorBrush,
                m_useRealizations ?
                    REALIZATION_RENDER_MODE_DEFAULT :
                    REALIZATION_RENDER_MODE_FORCE_UNREALIZED
                );
```



## <a name="requirements"></a><span data-ttu-id="599c5-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="599c5-118">Requirements</span></span>



| <span data-ttu-id="599c5-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="599c5-119">Requirement</span></span> | <span data-ttu-id="599c5-120">Wert</span><span class="sxs-lookup"><span data-stu-id="599c5-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="599c5-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="599c5-121">Library</span></span><br/> | <dl> <span data-ttu-id="599c5-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="599c5-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="599c5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="599c5-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="599c5-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="599c5-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="599c5-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="599c5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="599c5-126">**ID2D1SolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="599c5-126">**ID2D1SolidColorBrush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)
</dt> </dl>

 

