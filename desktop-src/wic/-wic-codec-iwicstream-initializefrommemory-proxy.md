---
description: Proxy Funktion für die InitializeFromMemory-Methode.
ms.assetid: 737526ac-fe79-4d53-83c5-33102f5ac67b
title: IWICStream_InitializeFromMemory_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fe034698635a35c098f6466712d17489f301dd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362772"
---
# <a name="iwicstream_initializefrommemory_proxy-function"></a>IWICStream \_ InitializeFromMemory- \_ Proxy Funktion

Proxy Funktion für die [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICStream_InitializeFromMemory_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ BYTE       *pbBuffer,
  _In_ DWORD      cbBufferSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) \** _

Zeiger auf dieses [_ *IWICStream* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) -Objekt.

</dd> <dt>

*pbBuffer* \[ in\]
</dt> <dd>

Typ: **Byte \** _

Zeiger auf den Puffer, der zum Initialisieren des Streams verwendet wird.

</dd> <dt>

_cbBufferSize * \[ in\]
</dt> <dd>

Typ: **DWORD**

Die Größe des Puffers.

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



 

 




