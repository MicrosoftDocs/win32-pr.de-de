---
description: IWICStream_InitializeFromMemory_Proxy - Proxyfunktion für die InitializeFromMemory-Methode.
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
ms.openlocfilehash: be3cec08f2ad3970d8860803cfb70970cf7b765b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097128"
---
# <a name="iwicstream_initializefrommemory_proxy-function"></a>IWICStream \_ InitializeFromMemory-Proxyfunktion \_

Proxyfunktion für die [**InitializeFromMemory-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory)

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

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\***

Zeiger auf dieses [**IWICStream-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)

</dd> <dt>

*pbBuffer* \[ In\]
</dt> <dd>

Typ: **BYTE \***

Zeiger auf den Puffer, der zum Initialisieren des Streams verwendet wird.

</dd> <dt>

*cbBufferSize* \[ In\]
</dt> <dd>

Typ: **DWORD**

Die Größe des Puffers.

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



 

 




