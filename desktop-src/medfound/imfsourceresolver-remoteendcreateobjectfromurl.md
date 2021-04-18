---
description: 'Remotable-Version der imfsourceresolver:: endkreateobjectfromurl-Methode.'
ms.assetid: 42764869-9cbc-4f41-a3af-f2d869db9f99
title: Remoteendkreateobjectfromurl (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fff650dca012b58dc6fd46b26f13b1c2ac3c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368141"
---
# <a name="remoteendcreateobjectfromurl"></a>Remoteendkreateobjectfromurl

Remotable-Version der [**imfsourceresolver:: endkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) -Methode.

``` syntax
[call_as(EndCreateObjectFromURL)]
HRESULT RemoteEndCreateObjectFromURL(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a>Bemerkungen

Anwendungen können diese Methode nicht direkt aufzurufen, und-Objekte implementieren diese Methode nicht. Die-Methode wird nicht in der vtable für die-Schnittstelle angezeigt. Wenn [**endkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) über Prozess Grenzen hinweg aufgerufen wird, übersetzt der Media Foundation Proxy/Stub-DLL den Aufruf in einen Aufruf der Remote Methode und übersetzt ihn anschließend wieder.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mfuuid. lib</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMF sourceresolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




