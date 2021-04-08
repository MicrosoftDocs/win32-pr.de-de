---
title: D1111 mit Schicht verwenden, wenn Clip ausreichend ist
ms.assetid: 07fe3c66-15be-408b-a30b-a7f52919c058
description: Eine Ebene wird mit einer NULL-Deckkraft Maske, 1,0 Deckkraft und einer durch Achsen ausgerichteten rechteckigen geometrischen Maske verwendet. Die Push-/Popout-API sollte die gleichen Ergebnisse erzielen, wenn Sie eine höhere Leistung erzielen.
keywords:
- D1111 Verwenden einer Schicht, wenn der Clip ausreichend ist Direct2D
topic_type:
- apiref
api_name:
- D1111 Using Layer When Clip Is Sufficient
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: a30bbfd7b8ca448928249018a28bc4d6a8a2f57f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730072"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a>D1111: Schicht verwenden, wenn Clip ausreichend ist

Perf: eine Ebene wird mit einer **null** -Deckkraft Maske, 1,0 Deckkraft und einer durch Achsen ausgerichteten rechteckigen geometrischen Maske verwendet. Die Push-/Popout-API sollte die gleichen Ergebnisse erzielen, wenn Sie eine höhere Leistung erzielen.

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*berfläche*
</dt> <dd>

Die Adresse der-Schnittstelle.

</dd> </dl> 

|             |             |
|-------------|-------------|
| Fehlerstufe | Information |



 

## <a name="examples"></a>Beispiele

Im folgenden Code werden die [**pushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) und [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) verwendet, wenn die Ebene nur ein primitiv (ein Rechteck) enthält und die Felder der [**D2D1 \_ Layer \_ Parameters**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) -Struktur auf Standardwerte festgelegt sind. Die Standardwerte der **D2D1 \_ Layer \_ Parameters** -Struktur finden Sie unter [**layerparameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



Dieses Beispiel erzeugt die folgende Debugmeldung:

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a>Mögliche Ursachen

Es wurde eine Ebene verwendet, wenn die [**pushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) -Methode und die [**popaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) -Methode nicht ausreichen.

 

 