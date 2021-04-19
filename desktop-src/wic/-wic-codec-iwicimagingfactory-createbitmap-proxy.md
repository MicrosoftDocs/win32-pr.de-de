---
description: Proxy Funktion für die Methode "kreatebitmap".
ms.assetid: 5647521b-231d-4819-97ab-4dfb5f796211
title: IWICImagingFactory_CreateBitmap_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 56684de0280ae27bf2ec1e900bd718faec4733fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373250"
---
# <a name="iwicimagingfactory_createbitmap_proxy-function"></a>IWICImagingFactory-Funktion zum Generieren von \_ \_ Funktionen

Proxy Funktion für die Methode " [**kreatebitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap) ".

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICImagingFactory_CreateBitmap_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  UINT                       uiWidth,
  _In_  UINT                       uiHeight,
  _In_  REFWICPixelFormatGUID      pixelFormat,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfactory* \[ in\]
</dt> <dd>

Typ: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_uiWidth * \[ in\]
</dt> <dd>

Typ: **uint**

Die Breite der neuen Bitmap.

</dd> <dt>

*uiheight* \[ in\]
</dt> <dd>

Typ: **uint**

Die Höhe der neuen Bitmap.

</dd> <dt>

*Pixel Format* \[ in\]
</dt> <dd>

Typ: **reberwicpixelformatguid**

Das Pixel Format der neuen Bitmap.

</dd> <dt>

*Option* \[ in\]
</dt> <dd>

Typ: **[ **wicbitmapkreatecacheoption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**

Die Cache Erstellungs Optionen der neuen Bitmap.

</dd> <dt>

*ppibitmap* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***

Ein Zeiger, der einen Zeiger auf die neue Bitmap empfängt.

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



 

 




