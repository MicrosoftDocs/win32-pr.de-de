---
description: Proxyfunktion für die GetDataPointer-Methode.
ms.assetid: 7256d6eb-cb7c-4067-8382-511d64da6825
title: IWICBitmapLock_GetDataPointer_STA_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetDataPointer_STA_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b693c78ba3a3d7c68c33f68ec1494997536ffb10272cc384d89d9e94ded7145b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206746"
---
# <a name="iwicbitmaplock_getdatapointer_sta_proxy-function"></a>IWICBitmapLock \_ \_ GetDataPointer-STA-Proxyfunktion \_

Proxyfunktion für die [**GetDataPointer-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapLock_GetDataPointer_STA_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbBufferSize,
  _Out_ BYTE           **ppbData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\***

Zeiger auf dieses [**IWICBitmapLock-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)

</dd> <dt>

*bluBufferSize* \[ out\]
</dt> <dd>

Typ: **UINT \***

Ein Zeiger, der die Größe des Puffers empfängt.

</dd> <dt>

*ppbData* \[ out\]
</dt> <dd>

Typ: **BYTE \* \***

Ein Zeiger, der einen Zeiger auf das linke obere Pixel im gesperrten Rechteck empfängt.

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



 

 




