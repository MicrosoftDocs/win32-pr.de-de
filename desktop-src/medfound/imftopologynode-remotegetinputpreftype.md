---
description: Remotable-Version der METHODE VONTOPTOPOLOGYNode::GetInputPrefType.
ms.assetid: b02cf739-97a9-4bb0-abb1-0da491857c50
title: RemoteGetInputPrefType (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cc11bbb28f15bad78955b59e556873d0500c92e45c126a9e710961ab83cf7e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878311"
---
# <a name="remotegetinputpreftype"></a>RemoteGetInputPrefType

Remotable-Version der [**METHODE VONTOPTOPOLOGYNode::GetInputPrefType.**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype)

``` syntax
[call_as(GetInputPrefType)] 
HRESULT RemoteGetInputPrefType(
    DWORD dwInputIndex,
    DWORD *pcbData,
    BYTE **ppbData
);
```

## <a name="remarks"></a>Hinweise

Anwendungen können diese Methode nicht direkt aufrufen, und Objekte implementieren diese Methode nicht. Die -Methode wird in der vtable für die -Schnittstelle nicht angezeigt. Wenn [**GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) über Prozessgrenzen hinweg aufgerufen wird, übersetzt die Media Foundation Proxy-/Stub-DLL den Aufruf in einen Aufruf der Remotemethode und übersetzt ihn dann zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mfuuid.lib</dt> </dl>                    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TOPOLOGYNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




