---
title: ActiveBasicDevice IsImageSupported-Eigenschaft (PlayToDevice.h)
description: Ruft einen Wert ab, der angibt, ob das Gerät Bilder unterstützt.
ms.assetid: FC53B87C-D739-4AD4-9DD3-415AC8692224
keywords:
- IsImageSupported-Eigenschaft Media Streaming-API
- IsImageSupported-Eigenschaft Media Streaming-API, ActiveBasicDevice-Schnittstelle
- ActiveBasicDevice-Schnittstelle Media Streaming-API, IsImageSupported-Eigenschaft
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsImageSupported
- ActiveBasicDevice.get_IsImageSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a147c5156f07c6cc6461cafcf8dc778013a7eb3048d1428f854b844d24f5642a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236711"
---
# <a name="activebasicdeviceisimagesupported-property"></a>ActiveBasicDevice::IsImageSupported (Eigenschaft)

Ruft einen Wert ab, der angibt, ob das Gerät Bilder unterstützt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_IsImageSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf einen **booleschen Wert, der angibt,** ob das Gerät Bilder unterstützt.

**TRUE,** wenn das Gerät Bilder unterstützt; andernfalls **FALSE.**

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

 

