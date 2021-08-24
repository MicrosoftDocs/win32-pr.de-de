---
description: Proxyfunktion für die CreateEncoder-Methode.
ms.assetid: e3ffad7f-eb0e-481d-81ee-caf18e14ba59
title: IWICImagingFactory_CreateEncoder_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateEncoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 20e1a95253c0943383842b9667d93e4fc98c48ab2abf229bae7c0b3ad3f3fe63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812280"
---
# <a name="iwicimagingfactory_createencoder_proxy-function"></a>IWICImagingFactory \_ \_ CreateEncoder-Proxyfunktion

Proxyfunktion für die [**CreateEncoder-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createencoder)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICImagingFactory_CreateEncoder_Proxy(
  _In_           IWICImagingFactory *pFactory,
  _In_           REFGUID            guidContainerFormat,
  _In_opt_ const GUID               *pguidVendor,
  _Out_          IWICBitmapEncoder  **ppIEncoder
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFactory* \[ In\]
</dt> <dd>

Typ: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*guidContainerFormat* \[ In\]
</dt> <dd>

Typ: **REFGUID**

Die GUID für das gewünschte Containerformat.

</dd> <dt>

*pguidVendor* \[ in, optional\]
</dt> <dd>

Typ: **const \* GUID**

Die Hersteller-GUID für den Encoder.

</dd> <dt>

*ppIEncoder* \[ out\]
</dt> <dd>

Typ: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\*\***

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



 

 




