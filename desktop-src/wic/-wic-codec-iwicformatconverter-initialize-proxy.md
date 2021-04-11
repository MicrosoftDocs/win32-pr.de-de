---
description: Proxy Funktion für die Initialize-Methode.
ms.assetid: 26112d52-95e2-4c67-83fc-cf5e28712730
title: IWICFormatConverter_Initialize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFormatConverter_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6450c1a508507db73e44ef8b88b4f94970ac6004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217666"
---
# <a name="iwicformatconverter_initialize_proxy-function"></a>IWICFormatConverter \_ Initialisieren der \_ Proxy Funktion

Proxy Funktion für die [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICFormatConverter_Initialize_Proxy(
  _In_ IWICFormatConverter   *THIS_PTR,
  _In_ IWICBitmapSource      *pISource,
  _In_ REFWICPixelFormatGUID dstFormat,
  _In_ WICBitmapDitherType   dither,
  _In_ IWICPalette           *pIPalette,
  _In_ double                alphaThresholdPercent,
  _In_ WICBitmapPaletteType  paletteTranslate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) \** _

Zeiger auf dieses [_ *IWICFormatConverter* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) -Objekt.

</dd> <dt>

*pisource* \[ in\]
</dt> <dd>

Typ: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Die zu konvertierende Eingabe Bitmap.

</dd> <dt>

_dstFormat * \[ in\]
</dt> <dd>

Typ: **reberwicpixelformatguid**

Die GUID des Ziel Pixel Formats.

</dd> <dt>

*Dithering* \[ in\]
</dt> <dd>

Typ: **[ **wicbitmapdithertype**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**

Der für die Konvertierung verwendete [**wicbitmapdithertype**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) .

</dd> <dt>

*pipalette* \[ in\]
</dt> <dd>

Typ: **[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Die für die Konvertierung zu verwendende Palette.

</dd> <dt>

_alphaThresholdPercent * \[ in\]
</dt> <dd>

Typ: **Double**

Der für die Konvertierung zu verwendende Alpha Schwellenwert.

</dd> <dt>

*palettetranslation* \[ in\]
</dt> <dd>

Typ: **[ **wicbitmappalettetype**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**

Der palettenübersetzungs Typ, der für die Konvertierung verwendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




