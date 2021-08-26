---
title: ID2D1RenderTarget CreateRadialGradientBrush-Methoden (D2d1.h)
description: Erstellt ein ID2D1RadialGradientBrush-Objekt, das zum Zeichnen von Bereichen mit einem radialen Farbverlauf verwendet werden kann.
ms.assetid: 985a4c1b-d29b-46ed-bc55-6dcd313718a8
keywords:
- CreateRadialGradientBrush-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b32c384e55f8c6ac17551c290c36e1130c05d5939fd5cf56116410ddac37320f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108820"
---
# <a name="id2d1rendertargetcreateradialgradientbrush-methods"></a>ID2D1RenderTarget::CreateRadialGradientBrush-Methoden

Erstellt ein [**ID2D1RadialGradientBrush-Objekt,**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) das zum Zeichnen von Bereichen mit einem radialen Farbverlauf verwendet werden kann.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                       | BESCHREIBUNG                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRadialGradientBrush(D2D1 \_ RADIAL GRADIENT BRUSH PROPERTIES \_ \_ \_&,ID2D1GradientStopCollection \* ,ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))                            | Erstellt einen [**ID2D1RadialGradientBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) der die angegebenen Farbverlaufsstopps enthält, über keine Transformation verfügt und über eine Basisdurchlässigkeit von 1,0 verfügt. <br/> |
| [**CreateRadialGradientBrush(D2D1 \_ RADIAL GRADIENT BRUSH PROPERTIES \_ \_ \_&,D2D1 \_ BRUSH PROPERTIES \_&,ID2D1GradientStopCollection \* ,ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))   | Erstellt einen [**ID2D1RadialGradientBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) der die angegebenen Farbverlaufsstopps und die angegebene Transformation und Basisdurchlässigkeit enthält. <br/> |
| [**CreateRadialGradientBrush(D2D1 \_ RADIAL GRADIENT BRUSH PROPERTIES \_ \_ \_ \* ,D2D1 \_ BRUSH PROPERTIES \_ \* ,ID2D1GradientStopCollection \* ,ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) | Erstellt einen [**ID2D1RadialGradientBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) der die angegebenen Farbverlaufsstopps und die angegebene Transformation und Basisdurchlässigkeit enthält. <br/> |



## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [How to Create a Radial Gradient Brush](how-to-create-a-radial-gradient-brush.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Erstellen eines Pinsels mit radialem Farbverlauf](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[Übersicht über Pinsel](direct2d-brushes-overview.md)
</dt> </dl>

�

�
