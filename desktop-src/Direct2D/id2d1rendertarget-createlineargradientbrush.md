---
title: ID2D1RenderTarget | atelineargradientbrush-Methoden (D2d1. h)
description: Erstellt ein ID2D1LinearGradientBrush-Objekt für das Zeichnen von Bereichen mit einem linearen Farbverlauf.
ms.assetid: dc07113f-ff93-4b0f-8328-02dd481dccb0
keywords:
- Methoden von "kreatelineargradientbrush" Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 428fcb44ddf50af7b3e78c28e359430bceee2f79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358300"
---
# <a name="id2d1rendertargetcreatelineargradientbrush-methods"></a>ID2D1RenderTarget:: | atelineargradientbrush-Methoden

Erstellt ein [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) -Objekt für das Zeichnen von Bereichen mit einem linearen Farbverlauf.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                       | BESCHREIBUNG                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreatelineargradientbrush" (D2D1 \_ lineare \_ Gradient- \_ Pinsel \_ Eigenschaften&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))                            | Erstellt ein [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) -Wert, der die angegebenen Farbverlaufs Stopps enthält, über keine Transformation verfügt und über eine Basis Deckkraft von 1,0 verfügt. <br/> |
| [**"Kreatelineargradientbrush" (D2D1 \_ lineare \_ Gradient- \_ Pinsel \_ Eigenschaften&, D2D1 \_ Brush- \_ Eigenschaften&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))   | Erstellt eine [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) , die die angegebenen Farbverlaufs Stopps enthält und über die angegebene Transformation und die angegebene Basis Deckkraft verfügt. <br/> |
| [**"Kreatelineargradientbrush" (D2D1 \_ lineare \_ Gradient- \_ Pinsel \_ Eigenschaften \* , D2D1 \_ Brush- \_ Eigenschaften \* , ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) | Erstellt eine [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) , die die angegebenen Farbverlaufs Stopps enthält und über die angegebene Transformation und die angegebene Basis Deckkraft verfügt. <br/> |



## <a name="examples"></a>Beispiele

Ein Beispiel, das zeigt, wie eine Auflistung von Farbverlaufs Stopps erstellt und zum Definieren eines linearen Farbverlaufs verwendet wird, finden Sie unter [Erstellen eines linearen Farbverlaufs Pinsels](how-to-create-a-linear-gradient-brush.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**"Kreategradientstopcollection"**](id2d1rendertarget-creategradientstopcollection.md)
</dt> <dt>

[**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)
</dt> <dt>

[**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)
</dt> <dt>

[**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)
</dt> <dt>

[Erstellen eines linearen Farbverlaufs Pinsels](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[Übersicht über Pinsel](direct2d-brushes-overview.md)
</dt> </dl>

�

�
