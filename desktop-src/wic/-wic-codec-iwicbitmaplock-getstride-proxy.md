---
description: Proxy Funktion für die getstride-Methode.
ms.assetid: 243439f3-2267-4632-b312-75c5ae5eddaa
title: IWICBitmapLock_GetStride_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetStride_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 70e42e233235b8616cf9191189ecc9e9ff01e85f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368982"
---
# <a name="iwicbitmaplock_getstride_proxy-function"></a>Iwicbitmaplock \_ getstride- \_ Proxy Funktion

Proxy Funktion für die [**getstride**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getstride) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapLock_GetStride_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbStride
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**iwicbitmaplock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _

Zeiger auf dieses [_ *iwicbitmaplock* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) -Objekt.

</dd> <dt>

*pcbstride* \[ vorgenommen\]
</dt> <dd>

Typ: **uint \** _

Der Bitmap-Schritt.

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



 

 




