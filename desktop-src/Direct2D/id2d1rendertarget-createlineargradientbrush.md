---
title: ID2D1RenderTarget CreateLinearGradientBrush-Methoden (D2d1.h)
description: Erstellt ein ID2D1LinearGradientBrush-Objekt zum Malen von Bereichen mit einem linearen Farbverlauf.
ms.assetid: dc07113f-ff93-4b0f-8328-02dd481dccb0
keywords:
- CreateLinearGradientBrush-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 74e3ba102b24b330f176189a66eae7ac9cd74ece194900f3d8997675bf486641
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966870"
---
# <a name="id2d1rendertargetcreatelineargradientbrush-methods"></a>ID2D1RenderTarget::CreateLinearGradientBrush-Methoden

Erstellt ein [**ID2D1LinearGradientBrush-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) zum Malen von Bereichen mit einem linearen Farbverlauf.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                       | Beschreibung                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateLinearGradientBrush(D2D1 \_ LINEAR GRADIENT BRUSH PROPERTIES \_ \_ \_&,ID2D1GradientStopCollection \* ,ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))                            | Erstellt einen [**ID2D1LinearGradientBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) der die angegebenen Farbverlaufsstopps enthält, über keine Transformation verfügt und über eine Basisdurchlässigkeit von 1,0 verfügt. <br/> |
| [**CreateLinearGradientBrush(D2D1 \_ LINEAR GRADIENT BRUSH PROPERTIES \_ \_ \_&,D2D1 \_ BRUSH PROPERTIES \_&,ID2D1GradientStopCollection \* ,ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))   | Erstellt einen [**ID2D1LinearGradientBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) der die angegebenen Farbverlaufsstopps enthält und über die angegebene Transformation und Basisdurchlässigkeit verfügt. <br/> |
| [**CreateLinearGradientBrush(D2D1 \_ LINEAR GRADIENT BRUSH PROPERTIES \_ \_ \_ \* ,D2D1 \_ BRUSH PROPERTIES \_ \* ,ID2D1GradientStopCollection \* ,ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) | Erstellt einen [**ID2D1LinearGradientBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) der die angegebenen Farbverlaufsstopps enthält und über die angegebene Transformation und Basisdurchlässigkeit verfügt. <br/> |



## <a name="examples"></a>Beispiele

Ein Beispiel, das zeigt, wie eine Farbverlaufsstoppsammlung erstellt und zum Definieren eines linearen Farbverlaufs verwendet wird, finden Sie unter [How to Create a Linear Gradient Brush](how-to-create-a-linear-gradient-brush.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**CreateGradientStopCollection**](id2d1rendertarget-creategradientstopcollection.md)
</dt> <dt>

[**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)
</dt> <dt>

[**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)
</dt> <dt>

[**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)
</dt> <dt>

[Erstellen eines Pinsels mit linearem Farbverlauf](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[Übersicht über Pinsel](direct2d-brushes-overview.md)
</dt> </dl>

�

�
