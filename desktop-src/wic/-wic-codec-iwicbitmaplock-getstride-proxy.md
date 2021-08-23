---
description: Proxyfunktion für die GetStride-Methode.
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
ms.openlocfilehash: 3d2635e58c8cce37a6744fe4101626c99556f5ad40fe98a88fc46fea06740edb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088383"
---
# <a name="iwicbitmaplock_getstride_proxy-function"></a>\_ \_ IWICBitmapLock-GetStride-Proxyfunktion

Proxyfunktion für die [**GetStride-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getstride)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapLock_GetStride_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbStride
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DIES \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\***

Zeiger auf dieses [**IWICBitmapLock-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)

</dd> <dt>

*pwStride* \[ out\]
</dt> <dd>

Typ: **UINT \***

Der Bitmapschritt.

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



 

 




