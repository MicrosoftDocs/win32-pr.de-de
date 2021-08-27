---
description: Remotable-Version von CISWorkQueueServicesEX::BeginRegisterPlatformWorkQueueWithMMCSSEx.
ms.assetid: 75af7ce6-9b74-4d61-b7f2-5d07538f91cf
title: RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1174e4edb8271aa9240857d8082ade87d1a8e6551ac788f98f217c41eb1d9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114290"
---
# <a name="remotebeginregisterplatformworkqueuewithmmcssex"></a>RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx

Remotable version of [**CISWorkQueueServicesEX::BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex).

``` syntax
[call_as(BeginRegisterPlatformWorkQueueWithMMCSSEx)]
HRESULT RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx(
    DWORD dwPlatformWorkQueue,
    LPCWSTR wszClass,
    DWORD dwTaskId, 
    LONG lPriority,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a>Hinweise

Anwendungen können diese Methode nicht direkt aufrufen, und Objekte implementieren diese Methode nicht. Die -Methode wird nicht in der vtable für die -Schnittstelle angezeigt. Wenn [**BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex) prozessübergreifend aufgerufen wird, übersetzt die Media Foundation-Proxy-/Stub-DLL den Aufruf in einen Aufruf der Remotemethode und übersetzt ihn dann zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Mfidl.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**VORARBEITQueueServicesEx**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
</dt> </dl>

 

 




