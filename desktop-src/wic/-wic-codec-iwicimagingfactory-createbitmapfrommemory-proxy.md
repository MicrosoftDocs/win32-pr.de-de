---
description: Proxyfunktion für die CreateBitmapFromMemory-Methode.
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
ms.openlocfilehash: e7f5567f2ead2b68440e448a9a03f36fdedceb5d31ecfc579f7df956988dfc01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033913"
---
# <a name="iwicimagingfactory_createbitmapfrommemory_proxy-function"></a>IWICImagingFactory \_ CreateBitmapFromMemory-Proxyfunktion \_

Proxyfunktion für die [**CreateBitmapFromMemory-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory)

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

*pFactory* \[ In\]
</dt> <dd>

Typ: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*uiWidth* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Breite der neuen Bitmap.

</dd> <dt>

*uiHeight* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Höhe der neuen Bitmap.

</dd> <dt>

*pixelFormat* \[ In\]
</dt> <dd>

Typ: **REFWICPixelFormatGUID**

Das Pixelformat der neuen Bitmap.

</dd> <dt>

*cbStride* \[ In\]
</dt> <dd>

Typ: **UINT**

Der [*Schritt der*](/windows) angegebenen Pixeldaten.

</dd> <dt>

*cbBufferSize* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Größe von *pbBuffer.*

</dd> <dt>

*pbBuffer* \[ In\]
</dt> <dd>

Typ: **BYTE \***

Der Puffer, der zum Erstellen der Bitmap verwendet wird.

</dd> <dt>

*ppIBitmap* \[ out\]
</dt> <dd>

Typ: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***

Ein Zeiger, der einen Zeiger auf die neue Bitmap empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

