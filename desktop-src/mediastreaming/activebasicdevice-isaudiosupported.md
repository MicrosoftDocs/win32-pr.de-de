---
title: ActiveBasicDevice IsAudioSupported-Eigenschaft (PlayToDevice.h)
description: Ruft einen Wert ab, der angibt, ob das Gerät Audio unterstützt.
ms.assetid: 22ABB97B-58E7-4C21-B359-C10DFC9C7194
keywords:
- IsAudioSupported-Eigenschaft Media Streaming-API
- IsAudioSupported-Eigenschaft Media Streaming-API, ActiveBasicDevice-Schnittstelle
- ActiveBasicDevice-Schnittstelle Media Streaming-API, IsAudioSupported-Eigenschaft
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsAudioSupported
- ActiveBasicDevice.get_IsAudioSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20125114b6cd134d153ad6425af5af410faf524714a2e505a37fbf57dcda21e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462423"
---
# <a name="activebasicdeviceisaudiosupported-property"></a>ActiveBasicDevice::IsAudioSupported-Eigenschaft

Ruft einen Wert ab, der angibt, ob das Gerät Audio unterstützt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_IsAudioSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf einen **booleschen Wert,** der angibt, ob das Gerät Audio unterstützt.

**TRUE,** wenn das Gerät Audio unterstützt; andernfalls **FALSE.**

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

 

