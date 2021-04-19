---
description: Proxy Funktion für die getminiatur-Methode.
ms.assetid: 377f8aac-3cdc-44dc-8c60-9b6bce915486
title: IWICBitmapFrameDecode_GetThumbnail_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c29b62b4d3839b7cd3db51574f38ab824b215310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356739"
---
# <a name="iwicbitmapframedecode_getthumbnail_proxy-function"></a>IWICBitmapFrameDecode \_ getminiatur- \_ Proxy Funktion

Proxy Funktion für die [**getminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapFrameDecode_GetThumbnail_Proxy(
  _In_  IWICBitmapFrameDecode *THIS_PTR,
  _Out_ IWICBitmapSource      **ppIThumbnail
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _

Zeiger auf dieses [_ *IWICBitmapFrameDecode* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Objekt.

</dd> <dt>

*ppiminiatur Ansicht* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***

Ein Zeiger, der einen Zeiger auf die [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) der Miniaturansicht empfängt.

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



 

 




