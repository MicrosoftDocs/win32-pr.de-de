---
description: Proxy Funktion für die GetMetadataQueryWriter-Methode.
ms.assetid: 64d2c6d8-f1dd-4397-8487-4d23c69aea82
title: IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 08ebc29691432ebed7b2a1eb01eecfcd109dbd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352675"
---
# <a name="iwicfastmetadataencoder_getmetadataquerywriter_proxy-function"></a>IWICFastMetadataEncoder \_ GetMetadataQueryWriter \_ Proxy-Funktion

Proxy Funktion für die [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _

Zeiger auf dieses [_ *IWICBitmapFrameDecode* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Objekt.

</dd> <dt>

*ppIMetadataQueryWriter* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***

Ein Zeiger, der einen Zeiger auf den Metadatenabfragewriter des Encoders empfängt.

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



 

 




