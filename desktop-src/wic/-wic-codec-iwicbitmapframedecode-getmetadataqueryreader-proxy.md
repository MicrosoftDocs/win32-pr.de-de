---
description: 'IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy-Funktion: Proxyfunktion für die GetMetadataQueryReader-Methode.'
ms.assetid: 2a3e0a59-3524-4da4-993a-607a3727faba
title: IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c6c00cc4463bd8540e5baeb41a10577e9f67e85c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091138"
---
# <a name="iwicbitmapframedecode_getmetadataqueryreader_proxy-function"></a>Proxyfunktion \_ "GetMetadataQueryReader" für IWICBitmapFrameDecode \_

Proxyfunktion für die [**GetMetadataQueryReader-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DIES \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***

Zeiger auf dieses [**IWICBitmapFrameDecode-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)

</dd> <dt>

*ppIMetadataQueryReader* \[ out\]
</dt> <dd>

Typ: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***

Ein Zeiger, der einen Zeiger auf einen [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




