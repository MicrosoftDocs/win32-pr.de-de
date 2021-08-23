---
description: Remotable-Version der METHODE "APKMediaStream::RequestSample".
ms.assetid: 05ed4de0-fe5c-4183-8f1d-55d5a27e436a
title: RemoteRequestSample (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b572a9de9a74a744b9a9fc2c31dd816900301da623869cecdb03820ccbcf1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034908"
---
# <a name="remoterequestsample"></a>RemoteRequestSample

Remotable-Version der [**METHODE "APKMediaStream::RequestSample".**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)

``` syntax
[call_as(RequestSample)]
HRESULT RemoteRequestSample();
```

## <a name="remarks"></a>Hinweise

Anwendungen können diese Methode nicht direkt aufrufen, und Objekte implementieren diese Methode nicht. Die -Methode wird in der vtable für die -Schnittstelle nicht angezeigt. Wenn [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) über Prozessgrenzen hinweg aufgerufen wird, übersetzt die Media Foundation Proxy-/Stub-DLL den Aufruf in einen Aufruf der Remotemethode und übersetzt ihn dann zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mfuuid.lib</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WFMEDIASTREAM**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)
</dt> </dl>

 

 




