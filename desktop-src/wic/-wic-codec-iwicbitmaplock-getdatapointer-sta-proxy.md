---
description: Proxy Funktion für die getdatapointer-Methode.
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
ms.openlocfilehash: 957ae5974d65430bd39ea41f2e094e9f9c7efb06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362745"
---
# <a name="iwicbitmaplock_getdatapointer_sta_proxy-function"></a>Iwicbitmaplock \_ getdatapointer \_ STA- \_ Proxy Funktion

Proxy Funktion für die [**getdatapointer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) -Methode.

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

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**iwicbitmaplock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _

Zeiger auf dieses [_ *iwicbitmaplock* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) -Objekt.

</dd> <dt>

*pcbbuffersize* \[ vorgenommen\]
</dt> <dd>

Typ: **uint \** _

Ein Zeiger, der die Größe des Puffers empfängt.

</dd> <dt>

_ppbData * \[ out\]
</dt> <dd>

Type: **Byte \* \***

Ein Zeiger, der einen Zeiger auf den oberen linken Pixel im gesperrten Rechteck empfängt.

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



 

 




