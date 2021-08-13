---
title: ActiveBasicDevice PhysicalNetworkInterface-Eigenschaft (PlayToDevice.h)
description: Ruft die ID der physischen Netzwerkschnittstelle ab.
ms.assetid: F426462F-CE26-4EE1-B679-A4C80B2919A5
keywords:
- PhysicalNetworkInterface-Eigenschaft Media Streaming-API
- PhysicalNetworkInterface-Eigenschaft Media Streaming-API, ActiveBasicDevice-Schnittstelle
- ActiveBasicDevice-Schnittstelle Media Streaming-API, PhysicalNetworkInterface-Eigenschaft
topic_type:
- apiref
api_name:
- ActiveBasicDevice.PhysicalNetworkInterface
- ActiveBasicDevice.get_PhysicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd9eb004607d93b92d502d22b253258bf39e501969e6b3952a58b0a03a1eec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736206"
---
# <a name="activebasicdevicephysicalnetworkinterface-property"></a>ActiveBasicDevice::P hysicalNetworkInterface-Eigenschaft

Ruft die ID der physischen Netzwerkschnittstelle ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_PhysicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine **GUID,** die die ID der physischen Netzwerkschnittstelle angibt.

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

 

