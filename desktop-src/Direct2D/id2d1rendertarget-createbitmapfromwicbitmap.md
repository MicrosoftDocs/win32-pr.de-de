---
title: ID2D1RenderTarget CreateBitmapFromWicBitmap-Methoden
description: Erstellt eine ID2D1Bitmap, indem die angegebene WIC-Bitmap (Microsoft Windows Imaging Component) kopiert wird.
ms.assetid: 463fc2f9-8ec6-47e8-8d48-a9015616e656
keywords:
- CreateBitmapFromWicBitmap-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 3d023db69afdc3cc69535d310cb21fb841c2f1bbe981df98e0aaa22074a46db0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119304340"
---
# <a name="id2d1rendertargetcreatebitmapfromwicbitmap-methods"></a>ID2D1RenderTarget::CreateBitmapFromWicBitmap-Methoden

Erstellt eine [**ID2D1Bitmap,**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) indem die angegebene WIC-Bitmap (Microsoft Windows Imaging Component) kopiert wird.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                              | BESCHREIBUNG                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateBitmapFromWicBitmap(IWICBitmapSource \* ,ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_id2d1bitmap))                                                       | Erstellt eine [**ID2D1Bitmap,**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) indem die angegebene WIC-Bitmap (Microsoft Windows Imaging Component) kopiert wird.<br/>  |
| [**CreateBitmapFromWicBitmap(IWICBitmapSource \* ,D2D1 \_ BITMAP PROPERTIES \_&,ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1__id2d1bitmap1))  | Erstellt eine [**ID2D1Bitmap,**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) indem die angegebene WIC-Bitmap (Microsoft Windows Imaging Component) kopiert wird.<br/> |
| [**CreateBitmapFromWicBitmap(IWICBitmapSource \* ,D2D1 \_ BITMAP PROPERTIES \_ \* ,ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap)) | Erstellt eine [**ID2D1Bitmap,**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) indem die angegebene WIC-Bitmap (Microsoft Windows Imaging Component) kopiert wird.<br/> |



## <a name="remarks"></a>Hinweise

Damit Direct2D ein WIC-Bild laden kann, muss es in ein unterstütztes Pixelformat und einen Alphamodus konvertiert werden. Eine Liste der unterstützten Pixelformate und Alphamodi finden Sie unter [Unterstützte Pixelformate und Alphamodi.](supported-pixel-formats-and-alpha-modes.md)

## <a name="examples"></a>Beispiele

Beispiele finden Sie unter [How to Load a Bitmap from a File (Laden einer Bitmap aus einer Datei)](how-to-load-a-direct2d-bitmap-from-a-file.md) und How to Load a Bitmap from a Resource [(Laden einer Bitmap aus einer Ressource).](how-to-load-a-bitmap-from-a-resource.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[Laden einer Bitmap aus einer Datei](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> <dt>

[Unterstützte Pixelformate und Alpha-Modi](supported-pixel-formats-and-alpha-modes.md)
</dt> </dl>

 

