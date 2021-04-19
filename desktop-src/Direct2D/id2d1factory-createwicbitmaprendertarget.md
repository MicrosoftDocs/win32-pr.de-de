---
title: ID2D1Factory-Methode für die Methode "deewicbitmaprendertarget"
description: Erstellt ein Renderziel, das in eine WIC-Bitmap (Microsoft Windows Imaging Component) gerendert wird.
ms.assetid: 93141743-c11d-40b4-83c5-07c9066836c7
keywords:
- Methoden von "kreatewicbitmaprendertarget" Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 4025028582c254e7a5724a575ef0d7f1c7d91570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369993"
---
# <a name="id2d1factorycreatewicbitmaprendertarget-methods"></a>ID2D1Factory:: | atewicbitmaprendertarget-Methoden

Erstellt ein Renderziel, das in eine WIC-Bitmap (Microsoft Windows Imaging Component) gerendert wird.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                            | BESCHREIBUNG                                                                                            |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**"Kreatewicbitmaprendertarget" (IWICBitmap \* , D2D1- \_ \_ Renderziel \_ Eigenschaften \* , ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) | Erstellt ein Renderziel, das in eine WIC-Bitmap (Microsoft Windows Imaging Component) gerendert wird.<br/> |
| [**"Kreatewicbitmaprendertarget" (IWICBitmap \* , D2D1 \_ \_ Renderziel \_ Eigenschaften&, ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))  | Erstellt ein Renderziel, das in eine WIC-Bitmap (Microsoft Windows Imaging Component) gerendert wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Anwendung sollte einmal Renderziele erstellen und Sie für die Lebensdauer der Anwendung oder bis zum D2DERR-Erstellungs [**\_ \_ Ziel**](direct2d-error-codes.md) Fehler erhalten. Wenn Sie diesen Fehler erhalten, müssen Sie das Renderziel (und alle erstellten Ressourcen) neu erstellen.

**Hinweis**   Diese Methode wird auf Windows Phone nicht unterstützt und schlägt fehl, wenn Sie auf einem Gerät mit dem Fehlercode 0x8899000b aufgerufen wird (für diesen Vorgang ist kein Hardware-renderinggerät verfügbar). Da der Windows Phone-Emulator Warp-Rendering unterstützt, schlägt diese Methode fehl, wenn Sie im Emulator mit einem anderen Fehlercode aufgerufen wird, 0x88982f80 (wincodec \_ Err \_ unsupportedpixelformat).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

