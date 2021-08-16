---
title: ActiveBasicDevice MaxVolume-Eigenschaft (PlayToDevice.h)
description: Ruft das maximale Volume ab, das vom Gerät unterstützt wird.
ms.assetid: EA0EC323-4A18-4CC1-8FA4-7BD302318863
keywords:
- MaxVolume-Eigenschaft Medienstreaming-API
- MaxVolume-Eigenschaft Medienstreaming-API , ActiveBasicDevice-Schnittstelle
- Media Streaming-API der ActiveBasicDevice-Schnittstelle, MaxVolume-Eigenschaft
topic_type:
- apiref
api_name:
- ActiveBasicDevice.MaxVolume
- ActiveBasicDevice.get_MaxVolume
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 803e2e66306bce0d6fd308501edece61668d5f2e0d8041273d508b662f6cd66f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736196"
---
# <a name="activebasicdevicemaxvolume-property"></a>ActiveBasicDevice::MaxVolume-Eigenschaft

Ruft das maximale Volume ab, das vom Gerät unterstützt wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MaxVolume(
  [out] boolean *UINT32
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf einen **UINT32,** der das maximale vom Gerät unterstützte Volume angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>PlayToDevice.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

