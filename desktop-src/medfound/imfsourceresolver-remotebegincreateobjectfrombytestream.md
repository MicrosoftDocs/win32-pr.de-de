---
description: Remotable-Version der METHODE "BESOURCEResolver::BeginCreateObjectFromByteStream".
ms.assetid: 960b5c51-b9b1-4956-a270-abfb7eedd482
title: RemoteBeginCreateObjectFromByteStream (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ac0365da83ec3f6bedc3ab45b9aef1458ed04c97ccdbfc1e00484824de47e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268980"
---
# <a name="remotebegincreateobjectfrombytestream"></a>RemoteBeginCreateObjectFromByteStream

Remotable-Version der [**METHODE "BESOURCEResolver::BeginCreateObjectFromByteStream".**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)

``` syntax
[call_as(BeginCreateObjectFromByteStream)]
HRESULT RemoteBeginCreateObjectFromByteStream(
    IMFByteStream* pByteStream,
    LPCWSTR pwszURL,
    IPropertyStore *pProps,
    DWORD dwFlags,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a>Hinweise

Anwendungen können diese Methode nicht direkt aufrufen, und Objekte implementieren diese Methode nicht. Die -Methode wird nicht in der vtable für die -Schnittstelle angezeigt. Wenn [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) prozessübergreifend aufgerufen wird, übersetzt die Media Foundation-Proxy-/Stub-DLL den Aufruf in einen Aufruf der Remotemethode und übersetzt ihn dann zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mfuuid.lib</dt> </dl>                    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**VERERBUNGQuelleResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




