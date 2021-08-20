---
description: Proxyfunktion für die CreateDecoderFromFileHandle-Methode.
ms.assetid: bc7f8a07-6d82-4d95-88ef-979d571758f4
title: IWICImagingFactory_CreateDecoderFromFileHandle_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFileHandle_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e9d2b67314ce3499f9cd3730159f7e267bd2b1890e678140d2688659620e501d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965209"
---
# <a name="iwicimagingfactory_createdecoderfromfilehandle_proxy-function"></a>IWICImagingFactory \_ CreateDecoderFromFileHandle-Proxyfunktion \_

Proxyfunktion für die [**CreateDecoderFromFileHandle-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFileHandle_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        ULONG_PTR          hFile,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFactory* \[ In\]
</dt> <dd>

Typ: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*hFile* \[ In\]
</dt> <dd>

Typ: **ULONG \_ PTR**

Das Dateihand handle, aus dem der Decoder erstellt werden soll.

</dd> <dt>

*pguidVendor* \[ In\]
</dt> <dd>

Typ: **const \* GUID**

Die Hersteller-GUID für den Decoder.

</dd> <dt>

*metadataOptions* \[ In\]
</dt> <dd>

Typ: **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**

Die [**WICDecodeOptions, die**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) beim Erstellen des Decoders verwendet werden.

</dd> <dt>

*ppIDecoder* \[ out\]
</dt> <dd>

Typ: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***

Ein Zeiger, der einen Zeiger auf einen neuen [**IWICBitmapDecoder empfängt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)

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



 

 




