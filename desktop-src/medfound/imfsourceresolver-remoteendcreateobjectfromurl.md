---
description: Die Remotable-Version der METHODE VONSOURCEResolver::EndCreateObjectFromURL.
ms.assetid: 42764869-9cbc-4f41-a3af-f2d869db9f99
title: RemoteEndCreateObjectFromURL (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c19951e9baedebb1713ad27faf8fa7848dad86eaea7ecefdd989b8cbd328783
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119229280"
---
# <a name="remoteendcreateobjectfromurl"></a>RemoteEndCreateObjectFromURL

Die Remotable-Version der [**METHODE VONSOURCEResolver::EndCreateObjectFromURL.**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl)

``` syntax
[call_as(EndCreateObjectFromURL)]
HRESULT RemoteEndCreateObjectFromURL(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a>Hinweise

Anwendungen können diese Methode nicht direkt aufrufen, und Objekte implementieren diese Methode nicht. Die -Methode wird in der vtable für die -Schnittstelle nicht angezeigt. Wenn [**EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) über Prozessgrenzen hinweg aufgerufen wird, übersetzt die Media Foundation Proxy-/Stub-DLL den Aufruf in einen Aufruf der Remotemethode und übersetzt ihn dann zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mfuuid.lib</dt> </dl>                    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SOURCEResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




