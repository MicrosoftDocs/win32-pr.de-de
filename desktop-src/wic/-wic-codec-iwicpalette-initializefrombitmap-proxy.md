---
description: Proxyfunktion für die InitializeFromBitmap-Methode.
ms.assetid: 9559a56d-7201-4b39-a3cd-9c0e4eac611a
title: IWICPalette_InitializeFromBitmap_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5c807e95b980a564096216727315f4a1534e8cd011cc78aa7322f670fff0876c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088182"
---
# <a name="iwicpalette_initializefrombitmap_proxy-function"></a>IWICPalette \_ \_ InitializeFromBitmap-Proxyfunktion

Proxyfunktion für die [**InitializeFromBitmap-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrombitmap)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICPalette_InitializeFromBitmap_Proxy(
  _In_ IWICPalette      *THIS_PTR,
  _In_ IWICBitmapSource *pISurface,
  _In_ UINT             colorCount,
  _In_ BOOL             fAddTransparentColor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DIES \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Zeiger auf dieses [**IWICPalette-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)

</dd> <dt>

*pISurface* \[ In\]
</dt> <dd>

Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Zeiger auf die Quellbitmap.

</dd> <dt>

*colorCount* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Anzahl der Farben, mit der die Palette initialisiert werden soll.

</dd> <dt>

*fAddTransparentColor* \[ In\]
</dt> <dd>

Typ: **BOOL**

Ein -Wert, der angibt, ob eine transparente Farbe hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




