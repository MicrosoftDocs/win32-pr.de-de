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
# <a name="d1111-using-layer-when-clip-is-sufficient"></a>D1111: Verwenden der Ebene, wenn clip ausreichend ist

PERF: Eine Ebene wird  mit einer NULL-Deckkraftmaske, einer Deckkraft von 1,0 und einer an einer Achse ausgerichteten rechteckigen geometrischen Maske verwendet. Die Push/Pop Clip-API sollte die gleichen Ergebnisse mit höherer Leistung erzielen.

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Schnittstelle*
</dt> <dd>

Die Adresse der Schnittstelle.

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| Fehlerstufe | Information |



 

## <a name="examples"></a>Beispiele

Im folgenden Code werden [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) und [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) verwendet, wenn die Ebene nur ein Primitiv (ein Rechteck) enthält und die Felder der [**D2D1 \_ LAYER \_ PARAMETERS-Struktur**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) auf Standardwerte festgelegt sind. Die Standardwerte der **D2D1 \_ LAYER \_ PARAMETERS-Struktur** finden Sie unter [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



In diesem Beispiel wird die folgende Debugmeldung erzeugt:

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a>Mögliche Ursachen

Eine Ebene wurde verwendet, wenn [**die Methoden PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) und [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) ausreichend waren.

 

 