---
description: Proxy Funktion für die Initialize-Methode.
ms.assetid: 0db79eb4-dcb2-491a-9bea-a0dec418f80f
title: IWICBitmapEncoder_Initialize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c1a2e684059b75e41c1d89e2d3dd5379cc208b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352470"
---
# <a name="iwicbitmapencoder_initialize_proxy-function"></a>Iwicbitmapcoder- \_ \_ Proxy Funktion initialisieren

Proxy Funktion für die [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapEncoder_Initialize_Proxy(
  _In_ IWICBitmapEncoder           *THIS_PTR,
  _In_ IStream                     *pIStream,
  _In_ WICBitmapEncoderCacheOption cacheOption
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _

Zeiger auf dieses [_ *iwicbitmapcoder* *](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) -Objekt.

</dd> <dt>

*pIStream* \[ in\]
</dt> <dd>

Typ: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _

Der Ausgabestream.

</dd> <dt>

_cacheOption * \[ in\]
</dt> <dd>

Typ: **[ **wicbitmapcodercacheoption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**

Die bei der Initialisierung verwendete [**wicbitmapcodercacheoption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) .

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



 

