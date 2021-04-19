---
title: ID2D1RenderTarget-Methode (Methode)
description: Erstellt ein ID2D1Bitmap-Element, indem die angegebene WIC-Bitmap (Microsoft Windows Imaging Component) kopiert wird.
ms.assetid: 463fc2f9-8ec6-47e8-8d48-a9015616e656
keywords:
- Methoden der Methode "Direct2D"
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 23ad055beab9f24c39f032a3e28456c231480c68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360274"
---
# <a name="id2d1rendertargetcreatebitmapfromwicbitmap-methods"></a>ID2D1RenderTarget:: kreatebitmapfromwicbitmap-Methoden

Erstellt ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) -Element, indem die angegebene WIC-Bitmap (Microsoft Windows Imaging Component) kopiert wird.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                              | BESCHREIBUNG                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreatebitmapfromwicbitmap" (IWICBitmapSource \* , ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_id2d1bitmap))                                                       | Erstellt ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) -Element, indem die angegebene WIC-Bitmap (Microsoft Windows Imaging Component) kopiert wird.<br/>  |
| [**"Kreatebitmapfromwicbitmap" (IWICBitmapSource \* , D2D1 \_ Bitmap \_ Properties&, ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1__id2d1bitmap1))  | Erstellt ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) -Element, indem die angegebene WIC-Bitmap (Microsoft Windows Imaging Component) kopiert wird.<br/> |
| [**"Kreatebitmapfromwicbitmap" (IWICBitmapSource \* , D2D1 \_ Bitmap \_ Properties \* , ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap)) | Erstellt ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) -Element, indem die angegebene WIC-Bitmap (Microsoft Windows Imaging Component) kopiert wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Bevor Direct2D ein WIC-Image laden kann, muss es in ein unterstütztes Pixel Format und einen Alpha-Modus konvertiert werden. Eine Liste der unterstützten Pixel Formate und Alpha Modi finden Sie [unter Unterstützte Pixel Formate und Alpha-Modi](supported-pixel-formats-and-alpha-modes.md).

## <a name="examples"></a>Beispiele

Beispiele finden Sie unter Gewusst [wie: Laden einer Bitmap aus einer Datei](how-to-load-a-direct2d-bitmap-from-a-file.md) und Gewusst [wie: Laden einer Bitmap aus einer Ressource](how-to-load-a-bitmap-from-a-resource.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[Laden einer Bitmap aus einer Datei](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> <dt>

[Unterstützte Pixelformate und Alpha-Modi](supported-pixel-formats-and-alpha-modes.md)
</dt> </dl>

 

