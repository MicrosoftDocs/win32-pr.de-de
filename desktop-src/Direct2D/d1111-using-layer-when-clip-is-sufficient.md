---
title: D1111 unter Verwendung der Ebene, wenn clip ausreichend ist
ms.assetid: 07fe3c66-15be-408b-a30b-a7f52919c058
description: Eine Ebene wird mit einer NULL-Deckkraftmaske, einer Deckkraft von 1,0 und einer achsenbündig ausgerichteten rechteckigen geometrischen Maske verwendet. Die Push/Pop Clip-API sollte die gleichen Ergebnisse mit höherer Leistung erzielen.
keywords:
- D1111 unter Verwendung der Ebene, wenn clip ausreichend direct2d ist
topic_type:
- apiref
api_name:
- D1111 Using Layer When Clip Is Sufficient
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e8463cc3940b69e326f13df6be9602dd6073fec0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549905"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a><span data-ttu-id="8d71c-105">D1111: Verwenden der Ebene, wenn clip ausreichend ist</span><span class="sxs-lookup"><span data-stu-id="8d71c-105">D1111: Using Layer When Clip Is Sufficient</span></span>

<span data-ttu-id="8d71c-106">PERF: Eine Ebene wird  mit einer NULL-Deckkraftmaske, einer Deckkraft von 1,0 und einer an einer Achse ausgerichteten rechteckigen geometrischen Maske verwendet.</span><span class="sxs-lookup"><span data-stu-id="8d71c-106">PERF - A layer is being used with a **NULL** opacity mask, 1.0 opacity, and an axis aligned rectangular geometric mask.</span></span> <span data-ttu-id="8d71c-107">Die Push/Pop Clip-API sollte die gleichen Ergebnisse mit höherer Leistung erzielen.</span><span class="sxs-lookup"><span data-stu-id="8d71c-107">The Push/Pop Clip API should achieve the same results with higher performance.</span></span>

## <a name="placeholders"></a><span data-ttu-id="8d71c-108">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="8d71c-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="8d71c-109"><span id="interface"></span><span id="INTERFACE"></span>*Schnittstelle*</span><span class="sxs-lookup"><span data-stu-id="8d71c-109"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="8d71c-110">Die Adresse der Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8d71c-110">The address of the interface.</span></span>

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| <span data-ttu-id="8d71c-111">Fehlerstufe</span><span class="sxs-lookup"><span data-stu-id="8d71c-111">Error Level</span></span> | <span data-ttu-id="8d71c-112">Information</span><span class="sxs-lookup"><span data-stu-id="8d71c-112">Information</span></span> |



 

## <a name="examples"></a><span data-ttu-id="8d71c-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d71c-113">Examples</span></span>

<span data-ttu-id="8d71c-114">Im folgenden Code werden [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) und [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) verwendet, wenn die Ebene nur ein Primitiv (ein Rechteck) enthält und die Felder der [**D2D1 \_ LAYER \_ PARAMETERS-Struktur**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) auf Standardwerte festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="8d71c-114">The following code uses the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) when the layer contains only one primitive (a rectangle) and the fields of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to defaults.</span></span> <span data-ttu-id="8d71c-115">Die Standardwerte der **D2D1 \_ LAYER \_ PARAMETERS-Struktur** finden Sie unter [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).</span><span class="sxs-lookup"><span data-stu-id="8d71c-115">For the default values of the **D2D1\_LAYER\_PARAMETERS** structure, see [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).</span></span>


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



<span data-ttu-id="8d71c-116">In diesem Beispiel wird die folgende Debugmeldung erzeugt:</span><span class="sxs-lookup"><span data-stu-id="8d71c-116">This example produces the following debug message:</span></span>

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a><span data-ttu-id="8d71c-117">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="8d71c-117">Possible Causes</span></span>

<span data-ttu-id="8d71c-118">Eine Ebene wurde verwendet, wenn [**die Methoden PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) und [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) ausreichend waren.</span><span class="sxs-lookup"><span data-stu-id="8d71c-118">A layer was used when the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) methods would have sufficed.</span></span>

 

 