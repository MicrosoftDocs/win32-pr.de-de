---
description: 'Remotable-Version der imfworkqueueservices:: beginunregisterplatformworkqueuewithmmcss-Methode.'
ms.assetid: c3117086-268e-4e52-acfb-2c8167adaa07
title: Remotebeginunregisterplatformworkqueuewithmmcss (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab364f041d6bc8d0f6275879c82a937e98f463b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355420"
---
# <a name="remotebeginunregisterplatformworkqueuewithmmcss"></a>Remotebeginunregisterplatformworkqueuewithmmcss

Remotable-Version der [**imfworkqueueservices:: beginunregisterplatformworkqueuewithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) -Methode.

``` syntax
[call_as(BeginUnregisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteBeginUnregisterPlatformWorkQueueWithMMCSS(
    DWORD dwPlatformWorkQueue,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a>Bemerkungen

Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht. Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt. Wenn [**beginunregisterplatformworkqueuewithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mfuuid. lib</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMF workqueueservices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




