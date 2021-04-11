---
description: Proxy Funktion für die initializefromistream-Methode.
ms.assetid: 3ab780bb-7fe7-4abe-9ea7-86f54ea15d91
title: IWICStream_InitializeFromIStream_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromIStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8d80a60d2a142b3c69c03b7352c81bcd0f5fc3ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217386"
---
# <a name="iwicstream_initializefromistream_proxy-function"></a>IWICStream \_ initializefromistream- \_ Proxy Funktion

Proxy Funktion für die [**initializefromistream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefromistream) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICStream_InitializeFromIStream_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ IStream    *pIStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) \** _

Zeiger auf dieses [_ *IWICStream* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) -Objekt.

</dd> <dt>

*pIStream* \[ in\]
</dt> <dd>

Typ: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _

Der Initialisierungs-Stream.

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



 

