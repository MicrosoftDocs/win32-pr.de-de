---
description: 'IWICFormatConverter_Initialize_Proxy-Funktion: Proxyfunktion für die Initialize-Methode.'
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
ms.openlocfilehash: d70d852adc8f810438ce46dc30345e68fa27e0fd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097158"
---
# <a name="iwicformatconverter_initialize_proxy-function"></a>IWICFormatConverter-Funktion \_ "Proxy initialisieren" \_

Proxyfunktion für die [**Initialize-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize)

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

*DIES \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\***

Zeiger auf dieses [**IWICFormatConverter-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)

</dd> <dt>

*pISource* \[ In\]
</dt> <dd>

Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Die zu konvertierende Eingabebitmap

</dd> <dt>

*dstFormat* \[ In\]
</dt> <dd>

Typ: **REFWICPixelFormatGUID**

Die Zielpixelformat-GUID.

</dd> <dt>

*Dither* \[ In\]
</dt> <dd>

Typ: **[ **WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**

Der für die Konvertierung verwendete [**WICBitmapDitherType.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)

</dd> <dt>

*pIPalette* \[ In\]
</dt> <dd>

Typ: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Die Palette, die für die Konvertierung verwendet werden soll.

</dd> <dt>

*alphaThresholdPercent* \[ In\]
</dt> <dd>

Typ: **double**

Der Alphaschwellenwert, der für die Konvertierung verwendet werden soll.

</dd> <dt>

*paletteTranslate* \[ In\]
</dt> <dd>

Typ: **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**

Der Für die Konvertierung zu verwendende Palettenübersetzungstyp.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




