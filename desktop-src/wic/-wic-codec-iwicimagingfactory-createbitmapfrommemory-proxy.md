---
description: Proxy Funktion für die Methode "kreatebitmapfrommemory".
ms.assetid: 5aa455d5-23e3-4738-b028-b84da0fb0c50
title: IWICImagingFactory_CreateBitmapFromMemory_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 79893952bb6dcdbab6c4a1cea4f57355831d31c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351025"
---
# <a name="iwicimagingfactory_createbitmapfrommemory_proxy-function"></a>IWICImagingFactory- \_ Funktion "endbitmapfrommemory" \_

Proxy Funktion für die Methode " [**kreatebitmapfrommemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) ".

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICImagingFactory_CreateBitmapFromMemory_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _In_  UINT                  uiWidth,
  _In_  UINT                  uiHeight,
  _In_  REFWICPixelFormatGUID pixelFormat,
  _In_  UINT                  cbStride,
  _In_  UINT                  cbBufferSize,
  _In_  BYTE                  *pbBuffer,
  _Out_ IWICBitmap            **ppIBitmap
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

*cbStride* \[ in\]
</dt> <dd>

Typ: **uint**

Der [*Schritt*](/windows) der angegebenen Pixeldaten.

</dd> <dt>

*cbBufferSize* \[ in\]
</dt> <dd>

Typ: **uint**

Die Größe von *pbBuffer*.

</dd> <dt>

*pbBuffer* \[ in\]
</dt> <dd>

Typ: **Byte \** _

Der zum Erstellen der Bitmap verwendete Puffer.

</dd> <dt>

_ppIBitmap * \[ out\]
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



 

