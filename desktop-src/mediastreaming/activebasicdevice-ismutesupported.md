---
title: ActiveBasicDevice IsMuteSupported-Eigenschaft (PlayToDevice.h)
description: Ruft einen Wert ab, der angibt, ob das Gerät das Stummschalten der Audiodaten unterstützt.
ms.assetid: FF4B533F-B416-4DBE-BF86-FA34E785FFA2
keywords:
- IsMuteSupported-Eigenschaft Media Streaming-API
- IsMuteSupported-Eigenschaft Media Streaming-API, ActiveBasicDevice-Schnittstelle
- ActiveBasicDevice-Schnittstelle Media Streaming-API, IsMuteSupported-Eigenschaft
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsMuteSupported
- ActiveBasicDevice.get_IsMuteSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fad8352504a6c950bb76206f05c77c5baa9f3baed2f1144a1d6c165e380a4b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236648"
---
# <a name="activebasicdeviceismutesupported-property"></a>ActiveBasicDevice::IsMuteSupported (Eigenschaft)

Ruft einen Wert ab, der angibt, ob das Gerät das Stummschalten der Audiodaten unterstützt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_IsMuteSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf einen **booleschen Wert,** der angibt, ob das Gerät das Stummschalten der Audiodaten unterstützt.

**TRUE,** wenn das Gerät das Stummschalten der Audiodaten unterstützt; andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>PlayToDevice.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

