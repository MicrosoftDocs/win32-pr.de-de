---
title: D1111 mit Ebene, wenn Clip ausreichend ist
ms.assetid: 07fe3c66-15be-408b-a30b-a7f52919c058
description: Eine Ebene wird mit einer NULL-Deckkraftmaske, 1,0 Deckkraft und einer an der Achse ausgerichteten rechteckigen geometrischen Maske verwendet. Die Push-/Pop-Clip-API sollte die gleichen Ergebnisse mit höherer Leistung erzielen.
keywords:
- D1111 mitHilfe der Ebene, wenn clip ausreichend Direct2D ist
topic_type:
- apiref
api_name:
- D1111 Using Layer When Clip Is Sufficient
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b03a6c2a4806724cd7cfdc97354e29e86dc60e0f1729ee9efeca89d971ca0a64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758100"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a>D1111: Verwenden der Ebene, wenn clip ausreichend ist

PERF: Eine Ebene wird  mit einer NULL-Deckkraftmaske, 1,0 Deckkraft und einer an einer Achse ausgerichteten rechteckigen geometrischen Maske verwendet. Die Push-/Pop-Clip-API sollte die gleichen Ergebnisse mit höherer Leistung erzielen.

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Schnittstelle*
</dt> <dd>

Die Adresse der Schnittstelle.

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| Fehlerstufe | Informationen |



 

## <a name="examples"></a>Beispiele

Im folgenden Code werden [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) und [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) verwendet, wenn die Ebene nur ein Primitives (ein Rechteck) enthält und die Felder der [**D2D1 \_ LAYER \_ PARAMETERS-Struktur**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) auf Standardwerte festgelegt sind. Die Standardwerte der **D2D1 \_ LAYER \_ PARAMETERS-Struktur** finden Sie unter [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).


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

Eine Ebene wurde verwendet, wenn die Methoden [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) und [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) ausreichen würden.

 

 