---
title: ID2D1RenderTarget CreateSolidColorBrush-Methoden (D2d1.h)
description: Erstellt einen neuen ID2D1SolidColorBrush, der zum Zeichnen von Bereichen mit volltonigen Farben verwendet werden kann.
ms.assetid: 3dbfe26f-cf36-47b0-925e-4934e0d7c390
keywords:
- CreateSolidColorBrush-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: c5d2b6ad86a63f584254fda20061179558653300a0d883f27477dd2b8ea2c2f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076890"
---
# <a name="id2d1rendertargetcreatesolidcolorbrush-methods"></a>ID2D1RenderTarget::CreateSolidColorBrush-Methoden

Erstellt einen neuen [**ID2D1SolidColorBrush,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__constd2d1_brush_properties__id2d1solidcolorbrush)) der zum Zeichnen von Bereichen mit volltonigen Farben verwendet werden kann.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateSolidColorBrush(D2D1 \_ COLOR \_ F&,ID2D1SolidColorBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__constd2d1_brush_properties__id2d1solidcolorbrush))                                                      | Erstellt eine neue [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__constd2d1_brush_properties__id2d1solidcolorbrush)) mit der angegebenen Farbe und einer Basisdurchlässigkeit von 1,0f. <br/> |
| [**CreateSolidColorBrush(D2D1 \_ COLOR \_ F&,D2D1 \_ BRUSH PROPERTIES \_&,ID2D1SolidColorBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__constd2d1_brush_properties__id2d1solidcolorbrush))   | Erstellt eine neue [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__constd2d1_brush_properties__id2d1solidcolorbrush)) mit der angegebenen Farbe und Deckkraft. <br/>                |
| [**CreateSolidColorBrush(D2D1 \_ COLOR F , \_ \* D2D1 \_ BRUSH PROPERTIES \_ \* ,ID2D1SolidColorBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__constd2d1_brush_properties__id2d1solidcolorbrush)) | Erstellt eine neue [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__constd2d1_brush_properties__id2d1solidcolorbrush)) mit der angegebenen Farbe und Deckkraft. <br/>                |



## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [Erstellen eines Volltonfarbpinsels.](how-to-create-a-solid-color-brush.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Übersicht über Pinsel](direct2d-brushes-overview.md)
</dt> <dt>

[Direct2D-Schnellstart](getting-started-with-direct2d.md)
</dt> </dl>

�

�