---
description: 'IWICBitmapEncoder_GetMetadataQueryWriter_Proxy-Funktion: Proxyfunktion für die GetMetadataQueryWriter-Methode.'
ms.assetid: 3186d473-f8a7-405a-8429-3f50104bee4a
title: IWICBitmapEncoder_GetMetadataQueryWriter_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 798a9b5bafb2f5011e42e603b8b2c98b0ba79b37
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091168"
---
# <a name="iwicbitmapencoder_getmetadataquerywriter_proxy-function"></a>IWICBitmapEncoder \_ GetMetadataQueryWriter-Proxyfunktion \_

Proxyfunktion für die [**GetMetadataQueryWriter-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapEncoder       *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***

Zeiger auf dieses [**IWICBitmapEncoder-Objekt.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)

</dd> <dt>

*ppIMetadataQueryWriter* \[ out\]
</dt> <dd>

Typ: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***

Ein Zeiger, der einen Zeiger auf einen [**IWICMetadataQueryWriter empfängt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)

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



 

 




