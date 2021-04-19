---
description: 'Remotable-Version der imfworkqueueservices:: beginregistertopologyworkqueueswithmmcss-Methode.'
ms.assetid: 1ea258c9-1f7f-4324-a17a-d044a4864ea4
title: Remotebeginregistertopologyworkqueueswithmmcss (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448008c29e34574263f04ebbc7dee54d60b6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357003"
---
# <a name="remotebeginregistertopologyworkqueueswithmmcss"></a>Remotebeginregistertopologyworkqueueswithmmcss

Remotable-Version der [**imfworkqueueservices:: beginregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) -Methode.

``` syntax
[call_as(BeginRegisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteBeginRegisterTopologyWorkQueuesWithMMCSS(
    IMFRemoteAsyncCallback *pCallback
); 
```

## <a name="remarks"></a>Bemerkungen

Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht. Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt. Wenn [**beginregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.

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

 

 




