---
description: 'Remotable-Version der imfpmphost:: forateobjectbyclsid-Methode.'
ms.assetid: be96be6d-47de-4d2b-81fc-13079de33888
title: Remotekreateobjectbyclsid (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e57307ece851484675d01a699037647efad771d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343738"
---
# <a name="remotecreateobjectbyclsid"></a>Remotekreateobjectbyclsid

Remotable-Version der [**imfpmphost:: forateobjectbyclsid**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) -Methode.

``` syntax
[call_as(CreateObjectByCLSID)]
HRESULT RemoteCreateObjectByCLSID( 
    REFCLSID clsid,
    BYTE *pbData, 
    DWORD cbData, 
    REFIID riid,
    void **ppv
);
```

## <a name="remarks"></a>Bemerkungen

Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht. Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt. Wenn " [**kreateobjectbyclsid**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) " über Prozess Grenzen hinweg aufgerufen wird, übersetzt die Media Foundation Proxy-/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt Sie dann zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mfuuid. lib</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imfpmphost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost)
</dt> <dt>

[PMP-Medien Sitzung](pmp-media-session.md)
</dt> <dt>

[Geschützter Medien Pfad](protected-media-path.md)
</dt> </dl>

 

 




