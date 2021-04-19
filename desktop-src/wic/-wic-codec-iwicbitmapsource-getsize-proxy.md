---
description: Proxy Funktion für die GetSize-Methode.
ms.assetid: a9b7d01c-78d9-47b8-a373-a7c49f7bccfd
title: IWICBitmapSource_GetSize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 978748125b7c7f643027077182b9136b577cb00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349902"
---
# <a name="iwicbitmapsource_getsize_proxy-function"></a>IWICBitmapSource \_ GetSize- \_ Proxy Funktion

Proxy Funktion für die [**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapSource_GetSize_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ UINT             *puiWidth,
  _Out_ UINT             *puiHeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Zeiger auf dieses [_ *IWICBitmapSource* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Objekt.

</dd> <dt>

*puiWidth* \[ vorgenommen\]
</dt> <dd>

Typ: **uint \** _

Ein Zeiger, der die Pixel Breite der Bitmap empfängt.

</dd> <dt>

_puiHeight * \[ out\]
</dt> <dd>

Typ: **uint \** _

Ein Zeiger, der die Pixelhöhe der Bitmap empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




