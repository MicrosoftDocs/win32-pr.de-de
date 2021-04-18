---
description: 'Remotable-Version der imfworkqueueservices:: endunregistertopologyworkqueueswithmmcss-Methode.'
ms.assetid: 8767a145-07b9-4427-9446-cee25e9074fa
title: Remoteendunregistertopologyworkqueueswithmmcss (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1131fcd920e306bc6d5f2954c283d41d61310f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347657"
---
# <a name="remoteendunregistertopologyworkqueueswithmmcss"></a>Remoteendunregistertopologyworkqueueswithmmcss

Remotable-Version der [**imfworkqueueservices:: endunregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) -Methode.

``` syntax
[call_as(EndUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndUnregisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a>Bemerkungen

Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht. Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt. Wenn [**endunregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.

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

 

 




