---
description: Remotable-Version der METHODE "MENUWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS".
ms.assetid: cb15129e-a3ad-4351-a7d6-dd4b883437bd
title: RemoteEndRegisterPlatformWorkQueueWithMMCSS (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14414d9fe6d093ee797d8c9e4879bd54cf89b3dbfc60b526ae8556f78ecc34e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878297"
---
# <a name="remoteendregisterplatformworkqueuewithmmcss"></a>RemoteEndRegisterPlatformWorkQueueWithMMCSS

Remotable-Version der [**METHODE "MENUWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS".**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss)

``` syntax
[call_as(EndRegisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndRegisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult,
    DWORD *pdwTaskId
);
```

## <a name="remarks"></a>Hinweise

Anwendungen können diese Methode nicht direkt aufrufen, und Objekte implementieren diese Methode nicht. Die -Methode wird in der vtable für die -Schnittstelle nicht angezeigt. Wenn [**EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) über Prozessgrenzen hinweg aufgerufen wird, übersetzt die Media Foundation Proxy-/Stub-DLL den Aufruf in einen Aufruf der Remotemethode und übersetzt ihn dann zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mfuuid.lib</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MENUWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




