---
description: Proxyfunktion für die CreateBitmap-Methode.
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
ms.openlocfilehash: 978946b5c22d8e4cb3427dbf27e5bb745efde259b48811a2b2a82e3721108184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965199"
---
# <a name="iwicimagingfactory_createbitmap_proxy-function"></a>IWICImagingFactory-Funktion \_ \_ "CreateBitmap-Proxy"

Proxyfunktion für die [**CreateBitmap-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap)

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

*Option* \[ In\]
</dt> <dd>

Typ: **[ **WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**

Die Optionen für die Cacheerstellung der neuen Bitmap.

</dd> <dt>

*ppIBitmap* \[ out\]
</dt> <dd>

Typ: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***

Ein Zeiger, der einen Zeiger auf die neue Bitmap empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows NUR XP mit SP2, Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




