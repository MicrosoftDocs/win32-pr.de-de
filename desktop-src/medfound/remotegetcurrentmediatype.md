---
description: 'Remotable-Version der imfmediatypeer Handler:: getcurrentmediatype-Methode.'
ms.assetid: f7f69adb-2a4a-47a9-bb92-ad9d005b962f
title: Remotegetcurrentmediatype (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc168198e8402d83538c046967d1d851ae2532b1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106349762"
---
# <a name="remotegetcurrentmediatype"></a>Remotegetcurrentmediatype

Remotable-Version der [**imfmediatypeer Handler:: getcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) -Methode.

``` syntax
[call_as(GetCurrentMediaType)]
HRESULT RemoteGetCurrentMediaType(
    BYTE **ppbData,
    DWORD *pcbData
);
```

## <a name="remarks"></a>Bemerkungen

Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht. Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt. Wenn [**getcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.

Diese Schnittstelle ist auf den folgenden Plattformen verfügbar, wenn die weitervertreibbaren Komponenten für das Windows Media-Format 11 SDK installiert sind:

-   Windows XP mit Service Pack 2 (SP2) und höher.
-   Windows XP Media Center Edition 2005 mit KB900325 (Windows XP Media Center Edition 2005) und KB925766 (Oktober 2006 Updaterollup für Windows XP Media Center Edition) ist installiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mfuuid. lib</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMF mediatypeer Handler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
</dt> </dl>

 

 




