---
title: ID2D1Factory CreateWicBitmapRenderTarget-Methoden
description: Erstellt ein Renderziel, das in einer Microsoft Windows Imaging Component (WIC)-Bitmap gerendert wird.
ms.assetid: 93141743-c11d-40b4-83c5-07c9066836c7
keywords:
- CreateWicBitmapRenderTarget-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 177f5459d8245292e2962e502882bb86643f3f8b777efd8a336fde5f8c671897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698180"
---
# <a name="id2d1factorycreatewicbitmaprendertarget-methods"></a>ID2D1Factory::CreateWicBitmapRenderTarget-Methoden

Erstellt ein Renderziel, das in einer Microsoft Windows Imaging Component (WIC)-Bitmap gerendert wird.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                            | BESCHREIBUNG                                                                                            |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**CreateWicBitmapRenderTarget(IWICBitmap \* ,D2D1 \_ RENDER TARGET PROPERTIES \_ \_ \* ,ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) | Erstellt ein Renderziel, das in einer Microsoft Windows Imaging Component (WIC)-Bitmap gerendert wird.<br/> |
| [**CreateWicBitmapRenderTarget(IWICBitmap \* ,D2D1 \_ RENDER TARGET PROPERTIES \_ \_&,ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))  | Erstellt ein Renderziel, das in einer Microsoft Windows Imaging Component (WIC)-Bitmap gerendert wird.<br/> |



## <a name="remarks"></a>Hinweise

Ihre Anwendung sollte Renderziele einmal erstellen und sie für die Lebensdauer der Anwendung oder bis zum Empfangen des [**Fehlers D2DERR \_ RECREATE \_ TARGET**](direct2d-error-codes.md) beibehalten. Wenn dieser Fehler angezeigt wird, müssen Sie das Renderziel (und alle erstellten Ressourcen) neu erstellen.

**Hinweis:**   Diese Methode wird auf Windows Phone nicht unterstützt und tritt beim Aufrufen auf einem Gerät mit dem Fehlercode 0x8899000b auf ( Für diesen Vorgang ist kein Hardwarerenderinggerät verfügbar). Da die Windows Phone Emulator WARP-Rendering unterstützt, tritt bei dieser Methode ein Fehler auf, wenn sie im Emulator mit einem anderen Fehlercode aufgerufen wird: 0x88982f80 (wincodec \_ err \_ unsupportedpixelformat).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

