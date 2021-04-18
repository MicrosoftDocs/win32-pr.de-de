---
description: Proxy Funktion für die Methode "kreatebitmapfromhbitmap".
ms.assetid: e4e9a6b4-00d9-4f87-aeec-f2c02c3f44ab
title: IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6599a9699e6fb83c1678cd0360f906cc8e0668c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351466"
---
# <a name="iwicimagingfactory_createbitmapfromhbitmap_proxy-function"></a>IWICImagingFactory- \_ Funktion "endbitmapfromhbitmap" \_

Proxy Funktion für die Methode " [**kreatebitmapfromhbitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap) ".

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy(
  _In_  IWICImagingFactory          *pFactory,
  _In_  HBITMAP                     hBitmap,
  _In_  HPALETTE                    hPalette,
  _In_  WICBitmapAlphaChannelOption options,
  _Out_ IWICBitmap                  **ppIBitmap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfactory* \[ in\]
</dt> <dd>

Typ: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_hBitmap * \[ in\]
</dt> <dd>

Typ: **hBitmap**

Ein Bitmap-Handle, aus dem die Bitmap erstellt werden soll.

</dd> <dt>

*hpalette* \[ in\]
</dt> <dd>

Typ: **hpalette**

Ein Palettenhandle, das zum Erstellen der Bitmap verwendet wird.

</dd> <dt>

*Optionen* \[ in\]
</dt> <dd>

Typ: **[ **wicbitmapalphachanneloption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**

Die Alphakanal Optionen zum Erstellen der Bitmap.

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



 

 




