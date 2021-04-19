---
description: Proxy Funktion für die GetMetadataQueryReader-Methode.
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
ms.openlocfilehash: e549fdfbacb5bd508a442c70c203595b8819750f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348983"
---
# <a name="iwicbitmapframedecode_getmetadataqueryreader_proxy-function"></a>IWICBitmapFrameDecode \_ GetMetadataQueryReader \_ Proxy-Funktion

Proxy Funktion für die [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _

Zeiger auf dieses [_ *IWICBitmapFrameDecode* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Objekt.

</dd> <dt>

*ppIMetadataQueryReader* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***

Ein Zeiger, der einen Zeiger auf eine [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)empfängt.

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



 

 




