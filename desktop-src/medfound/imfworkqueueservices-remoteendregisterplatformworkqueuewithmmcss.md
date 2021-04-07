---
description: 'Remotable-Version der imfworkqueueservices:: endregisterplatformworkqueuewithmmcss-Methode.'
ms.assetid: cb15129e-a3ad-4351-a7d6-dd4b883437bd
title: Remoteendregisterplatformworkqueuewithmmcss (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673281a8ed4e4c4174ecd2d874e7032776ea44c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749200"
---
# <a name="remoteendregisterplatformworkqueuewithmmcss"></a>Remoteendregisterplatformworkqueuewithmmcss

Remotable-Version der [**imfworkqueueservices:: endregisterplatformworkqueuewithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) -Methode.

``` syntax
[call_as(EndRegisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndRegisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult,
    DWORD *pdwTaskId
);
```

## <a name="remarks"></a>Bemerkungen

Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht. Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt. Wenn [**endregisterplatformworkqueuewithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.

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

 

 




